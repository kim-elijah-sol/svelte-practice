<script lang="ts">
    let src = "https://static-00.iconduck.com/assets.00/svelte-icon-1703x2048-c1sw8yt9.png"

    let alt = "Svelte Icon"
</script>

<h1>
    Dynamic Attributes
</h1>

<!-- src : attribute 명과 변수명이 동일하다면 short hand 사용 가능 -->
<!-- alt : 동적으로 변수를 사용하기 위해 {$변수명} 사용 -->
<img {src} alt="{alt} 입니다.">

<style>
    img {
        width: 200px;
    }
</style>