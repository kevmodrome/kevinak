<script>
  import TileWithBackground from "../components/common/TileWithBackground.svelte";
</script>

<style>
  .container {
    margin-right: 15px;
  }
  @media (min-width: 400px) {
    .container {
      margin-right: 35px;
    }
  }
  @media (min-width: 1080px) {
    .container {
      margin-right: 50px;
    }
  }

  img {
    width: 100%;
    height: 750px;
    object-fit: cover;
  }
</style>

<svelte:head>
  <title>Kevin Åberg Kultalahti's Personal Website</title>
</svelte:head>

<div class="container">
  <TileWithBackground>
    <img src="test.jpg" alt="" />
  </TileWithBackground>
</div>
