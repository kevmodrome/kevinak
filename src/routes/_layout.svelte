<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";

  export let segment;
</script>

<style>
  :global(html) {
    /* Allows content to fill the viewport and go beyond the bottom */
    height: 100%;

    /* Allows you to scroll below the viewport; default value is visible */
    overflow-y: scroll;

    /* To smooth any scrolling behavior */
    -webkit-overflow-scrolling: touch;
  }
  :global(body) {
    /* Allows content to fill the viewport and go beyond the bottom */
    height: 100%;

    /* Allows you to scroll below the viewport; default value is visible */
    overflow-y: scroll;
    overflow-x: hidden;

    /* To smooth any scrolling behavior */
    -webkit-overflow-scrolling: touch;
  }
  :global(h1) {
    font-family: "Merriweather", serif;
    font-size: 24px;
    font-weight: bold;
    color: #353f99;
  }
  :global(h2) {
    font-family: "Merriweather", serif;
    font-size: 24px;
    font-weight: normal;
    color: #353f99;
  }
  :global(h3) {
    font-family: "Merriweather", serif;
    font-size: 20px;
    font-weight: bold;
    color: #353f99;
  }
  :global(h4) {
    font-family: "Merriweather", serif;
    font-size: 20px;
    font-weight: bold;
  }
  :global(h5) {
    font-family: "Merriweather", serif;
    font-size: 16px;
    font-weight: bold;
  }
  :global(p) {
    font-family: "Open Sans";
    font-size: 18px;
    font-weight: normal;
  }
  :global(button) {
    font-family: "Open Sans";
    font-weight: normal;
  }
  :global(a) {
    color: #353f99;
    font-weight: bold;
    text-decoration: none;
  }
  :global(a:visited) {
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
<Footer />
