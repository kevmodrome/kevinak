<script>
  import TileWithBackground from "../components/common/TileWithBackground.svelte";
  import Tile from "../components/common/Tile.svelte";
  import Divider from "../components/common/Divider.svelte";
</script>

<style>
  .container {
    margin-right: 15px;
    margin-bottom: 100px;
  }
  @media (min-width: 500px) {
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
    object-fit: cover;
    height: 50vh;
  }
  @media (min-width: 500px) {
    img {
      height: 55vh;
    }
  }
  @media (min-width: 1080px) {
    img {
      height: 60vh;
    }
  }
  h1 {
    max-width: 700px;
    margin: 0 auto;
    text-align: center;
    color: #353f99;
    font-size: 24px;
  }
</style>

<svelte:head>
  <title>Kevin Åberg Kultalahti's Personal Website</title>
</svelte:head>

<div class="container">
  <TileWithBackground>
    <img src="test.jpg" alt="" />
  </TileWithBackground>
  <Tile>
    <h1>
      Hello, I’m Kevin, a React Native developer based in Stockholm, Sweden.
    </h1>
  </Tile>
  <Divider />
  <Tile>
    <div class="about">
      <img src="about.png" alt="Image of me doing coding." />
    </div>
    <div class="about-text">
      <h2>About Me</h2>
      <p>
        Eget montes, molestie sapien morbi vitae, ipsum. Viverra bibendum amet
        metus malesuada mus arcu ut turpis. Iaculis fames aenean nisi, id
        dignissim morbi cursus. Hendrerit eget lobortis diam adipiscing.
        Consectetur velit nec lacus, habitant. Nunc platea vel congue platea.
        Enim purus integer est a gravida faucibus metus.
      </p>
      <p>
        Fringilla in lorem rhoncus senectus fermentum, augue in suspendisse
        nulla. Et quis urna volutpat amet, dui lacus. Vulputate dignissim
        convallis egestas mauris diam egestas. Quam risus at ut massa. Enim
        pulvinar elit viverra nunc tincidunt velit. Tellus interdum dolor
        tristique.
      </p>
    </div>
  </Tile>
</div>
