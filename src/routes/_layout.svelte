<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  .container {
    margin: 0 auto;
    padding: 0 120px;
    max-width: 1200px;
  }
  main {
    background-color: green;
    width: 100%;
    box-sizing: border-box;
  }
</style>

<div class="container">
  <Nav {segment} />

  <main>
    <slot />
  </main>
</div>
