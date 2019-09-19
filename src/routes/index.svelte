<script>
  import TileWithBackground from "../components/common/TileWithBackground.svelte";
  import Tile from "../components/common/Tile.svelte";
  import Divider from "../components/common/Divider.svelte";

  import About from "../components/home/About.svelte";
  import Client from "../components/home/Client.svelte";
</script>

<style>
  .container {
    margin-bottom: 100px;
    margin: 0 auto;
  }

  .more-work {
    margin-top: 20px;
    display: flex;
    justify-content: flex-end;
  }

  .hover-effect {
    position: relative;
    font-weight: bold;
    text-decoration: none;
    padding: 1em 0;
    display: block;
  }

  .hover-effect:hover:before {
    right: auto;
    width: 100%;
  }

  .hover-effect:visited {
    color: black;
  }

  .hover-effect:before {
    content: "";
    position: absolute;
    width: 0%;
    height: 3px;
    bottom: 13px;
    left: 0;
    background-color: #353f99;
    transition: all 0.2s ease-in-out 0s;
  }

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

<svelte:head>
  <title>Kevin Åberg Kultalahti's Personal Website</title>
</svelte:head>

<div class="container">
  <TileWithBackground>
    <img src="test.jpg" alt="A picture of me." />
  </TileWithBackground>
  <Tile>
    <h1>
      Hello, I’m Kevin, a React Native developer based in Stockholm, Sweden.
    </h1>
  </Tile>
  <Divider />
  <About />
  <Divider />
  <Tile>
    <h2>Work</h2>
    <Client />
    <Client />
    <div class="more-work">
      <a class="hover-effect" href="/"><h3>See more of my work &#8594</h3></a>
    </div>
  </Tile>
</div>
