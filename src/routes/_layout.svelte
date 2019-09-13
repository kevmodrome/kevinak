<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  :global(h1) {
    font-family: "Merriwheather";
    font-size: 24px;
    font-weight: bold;
    color: #353f99;
  }
  :global(h2) {
    font-family: "Merriwheather";
    font-size: 24px;
    font-weight: normal;
    color: #353f99;
  }
  :global(h3) {
    font-family: "Merriwheather";
    font-size: 24px;
    font-weight: bold;
    color: #353f99;
  }
  :global(p) {
    font-family: "Open-sans";
    font-size: 18px;
    font-weight: normal;
  }
  :global(a) {
    color: #353f99;
  }

  .container {
    margin: 0 auto;
    padding: 0 20px;
    max-width: 1200px;
  }
  @media (min-width: 500px) {
    .container {
      padding: 0 40px;
    }
  }
  @media (min-width: 1080px) {
    .container {
      padding: 0 60px;
    }
  }
  main {
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
