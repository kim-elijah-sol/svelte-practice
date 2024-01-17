<script lang="ts">
    let list = getList()

    function randomError() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                if (Math.random() > 0.5) {
                    resolve('success')
                } else {
                    reject('Random Error')
                }
            }, 1000)
        })
    }

    async function getList (){
        await randomError()
        const res = await fetch('https://jsonplaceholder.typicode.com/todos')
        const data = await res.json()

        return data
    }

    function handleClick() {
        list = getList()
    }
</script>

<div>
    <button on:click={handleClick}>
        Re-try
    </button>
</div>

{#await list}
    <p>Data Loading...</p>
{:then data} 
    <ul>
        {#each data as item}
            <li>{item.title}</li>
        {/each}
    </ul>
{:catch error}
    <p style="color: red;">{error}</p>
{/await}
