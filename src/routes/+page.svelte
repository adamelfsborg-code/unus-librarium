<script lang="ts">
    let count: number = $state(0)

    const doubleCount = () => {
        return count * 2
    }

    let doubled: number = $derived(doubleCount())

    const incroment = () => {
        count += 1; 
    }

    $effect(() => {
        console.log({count, doubled})
    })
</script>

<div>
    <button type="button" on:click={incroment} >
        {count} * 2 = {doubled}
    </button>
</div>