<script>
  export let image;
  export let title;
  import TileWithBackground from "../common/TileWithBackground.svelte";
  import Tile from "../common/Tile.svelte";
</script>

<style>
  img {
    width: 100%;
    max-height: 50vh;
    object-fit: cover;
  }
  h1 {
    max-width: 700px;
    text-align: center;
    margin: 0 auto;
  }
  @media (min-width: 500px) {
    img {
      max-height: 55vh;
    }
    h1 {
      font-size: 18px;
    }
  }
  @media (min-width: 1080px) {
    img {
      max-height: 60vh;
    }
    h1 {
      font-size: 24px;
    }
  }
</style>

{#if image}
  <TileWithBackground>
    <img src="test.jpg" alt="A picture of me." />
  </TileWithBackground>
{/if}
<Tile>
  <h1>{title}</h1>
</Tile>
