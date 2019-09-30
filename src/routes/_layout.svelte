<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";

  export let segment;
</script>

<style>
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
<Footer />
