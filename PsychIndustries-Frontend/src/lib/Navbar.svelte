<script>
    import Test1 from "../pages/Test1.svelte";
    import Test2 from "../pages/Test2.svelte";

    export let menu = 1;
</script>

<style>
    ul#menu li{
        display : inline;
    }
</style>

<ul id="menu">
    <li><a href="/" on:click|preventDefault={() => (menu = 1)}>Test1</a></li> |
    <li><a href="/" on:click|preventDefault={() => (menu = 2)}>Test2</a></li>
</ul>

{#if menu === 1}
    <Test1 />
{:else if menu === 2}
    <Test2 />
{:else}
    <h1>
        Page Not Found
    </h1>
{/if}

