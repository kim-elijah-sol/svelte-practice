<script lang="ts">

    // svelte 는 react, vue 와 다르게 let, const 문법으로 상태를 선언할 수 있다.
    let count = 0;

    function handleClick () {
        count += 1;
    }
</script>

<button on:click={handleClick}>
    {count} 번 클릭했어요.
</button>