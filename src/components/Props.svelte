<script lang="ts">
    // export 로 내보내면 props 로 받을 수 있다.
    // = $defaultValue 로 기본 값을 지정할 수 있다.
    export let name: string = 'sol'
    export let age: number
    export let job: string
</script>

<h1>{name}님 안녕하세요!</h1>
<p>{age} 살 이시네요?</p>
<p>{job} 이시구요.</p>

<!-- $$props 를 사용해서 모든 props 를 사용할 수 있다. -->
<p>
    {JSON.stringify($$props)}
</p>
