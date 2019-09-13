<script>
  import TileWithBackground from "../components/common/TileWithBackground.svelte";
</script>

<style>
  .container {
    margin-right: 20px;
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
