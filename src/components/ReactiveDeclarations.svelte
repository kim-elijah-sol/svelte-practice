<script lang="ts">

    let count = 0;

    /**
     * $: 를 사용하여 reactive declaration 을 만들 수 있다.
     * reactive declaration 은 변수가 변경될 때마다 자동으로 실행된다.
     */
    $: doubled = count * 2;
    $: quadrupled = doubled * 2;

    function handleClick () {
        count += 1;
    }
</script>

<button on:click={handleClick}>
    {count} 번 클릭했어요.
</button>

<p>
    {count} * 2 = {doubled}
</p>

<p>
    {doubled} * 2 = {quadrupled}
</p>