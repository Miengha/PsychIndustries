<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import Navbar from "./lib/Navbar.svelte";

  let name = "Miengha";

  $: uppercaseName = name.toUpperCase();

  function changeName(event) {
    name = event.target.value;
  }
</script>

<main>
  <Navbar />
  <div>
    <h1>{uppercaseName}</h1>
<!--    <input type="text" value="{name}" on:input={changeName} />-->

    <input type="text" bind:value="{name}"/>

    <!--    <button on:click={changeName}>Change Name</button>-->

  <div class="card">
    <Counter />
  </div>
  </div>

</main>

<style>

</style>
