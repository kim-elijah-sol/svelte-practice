<script lang="ts">
    let count: number = 0;

    function increment() {
        count += 1;
    }
</script>

<div>
    <button on:click={increment}>+ 1</button>

    <p>{count}</p>

    {#if count % 2 === 0}
        <p>짝수</p>
    {:else}
        <p>홀수</p>
    {/if}
</div>