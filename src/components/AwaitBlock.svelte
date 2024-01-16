<script lang="ts">
    let list = getList()

    async function getList (){
        const res = await fetch('https://jsonplaceholder.typicode.com/todos')
        const data = await res.json()

        return data
    }
</script>


{#await list}
    <p>Data Loading...</p>
{:then data} 
    <ul>
        {#each data as item}
            <li>{item.title}</li>
        {/each}
    </ul>
{/await}
