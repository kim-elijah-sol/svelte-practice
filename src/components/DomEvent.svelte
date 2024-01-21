<script lang="ts">
    let p = { x: 0, y: 0 };

    function handleMousemove(event: MouseEvent) {
        p = {
            x: event.clientX,
            y: event.clientY
        }
    }
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<div on:mousemove={handleMousemove}>
	The mouse position is {p.x} x {p.y}
</div>

<style>
    div {
        width: 100%;
        height: 500px;
        background-color: #eee;
    }
</style>