<script lang="ts">
    type Skill = {
        name: string
        year: number
    }

    let mySkills: Skill[] = [
        {
            name: 'html',
            year: 5
        },
        {
            name: 'css',
            year: 5
        },
        {
            name: 'javascript',
            year: 4
        },
        {
            name: 'react',
            year: 4
        },
        {
            name: 'typescript',
            year: 3
        },
    ]
</script>

<ul>
    <!-- each block 은 반복문을 의미한다. -->
    <!-- ${배얄 데이터} as item 으로 선언한다. -->
    <!-- item 이 object 인 경우 비구조화 할당으로 선언할 수 있다. -->
    <!-- item 다음 데이터로는 index 값이 주어진다. -->
    {#each mySkills as { name, year }, index}
        <li>{index + 1} : {name} - {year}년차</li>
    {/each}
</ul>