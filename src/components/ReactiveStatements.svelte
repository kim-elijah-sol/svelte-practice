<script lang="ts">

    let count = 0;

    $: if (count >= 10) {
        alert(`count 값은 10을 넘을 수 없어요!`);
        count = 9;
    }

    function handleClick () {
        count += 1;
    }
</script>

<button on:click={handleClick}>
    {count} 번 클릭했어요.
</button>