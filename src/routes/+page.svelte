<script lang="ts">
	import AwaitBlock from './../components/AwaitBlock.svelte';
	import IfBlock from './../components/IfBlock.svelte';
	import ReactiveAssignments from './../components/ReactiveAssignments.svelte';
    import ReactiveDeclarations from './../components/ReactiveDeclarations.svelte';
    import ReactiveStatements from './../components/ReactiveStatements.svelte';
    import DynamicAttributes from '../components/DynamicAttributes.svelte';
    import Style from '../components/Style.svelte'
    import HtmlTag from '../components/HtmlTag.svelte'
    import Props from '../components/Props.svelte'
    import EachBlock from '../components/EachBlock.svelte'

    const components = [
        'dynamic attributes', 'style', 'html tag', 'reactive assignments', 'reactive declarations',
        'reactive statements', 'props', 'if block', 'each block', 'await block',
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

{#if checkedComponent === "reactive assignments"}
    <ReactiveAssignments />
{/if}

{#if checkedComponent === "reactive declarations"}
    <ReactiveDeclarations />
{/if}

{#if checkedComponent === "reactive statements"}
    <ReactiveStatements />
{/if}

<!-- react 와 같이 object literal 로 props 를 전달할 수 있다. -->
{#if checkedComponent === "props"}
    <Props {...{ age: 26, job: 'fe developer' }} />
{/if}

{#if checkedComponent === "if block"}
    <IfBlock />
{/if}

{#if checkedComponent === "each block"}
    <EachBlock />
{/if}

{#if checkedComponent === "await block"}
    <AwaitBlock />
{/if}