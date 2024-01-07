<script lang="ts">
    import DynamicAttributes from '../components/DynamicAttributes.svelte';
    import Style from '../components/Style.svelte'
    import HtmlTag from '../components/HtmlTag.svelte'

    const components = [
        'dynamic attributes', 'style', 'html tag',
    ] as const

    let checkedComponent: string = 'dynamic attributes';
</script>

{#each components as component}
    <label>
        <input
            type="radio"
            bind:group={checkedComponent}
            value={component}
        />
        {component}
    </label>
{/each}

{#if checkedComponent === "dynamic attributes"}
    <DynamicAttributes />
{/if}
    
{#if checkedComponent === "style"}
    <Style />
{/if}

{#if checkedComponent === "html tag"}
    <HtmlTag />
{/if}