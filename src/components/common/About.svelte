<script>
  export let title;
  export let reverse;
  import Tile from "../common/Tile.svelte";
</script>

<style>
  .container {
    display: flex;
    flex-direction: column-reverse;
    max-width: 800px;
    margin: 0 auto;
  }
  .image {
    flex: 1;
    margin-top: 20px;
  }
  .text {
    flex: 1;
  }
  img {
    width: 100%;
    max-height: 500px;
    max-height: 300px;
    object-fit: cover;
  }
  @media (min-width: 500px) {
    img {
      height: 100%;
    }
    .container {
      flex-direction: row;
    }
    .reverse {
      flex-direction: row-reverse;
    }
    .image {
      flex: 1;
      margin-top: 0px;
      margin-right: 20px;
    }
    .text {
      flex: 2;
    }
  }
  @media (min-width: 1080px) {
    img {
      height: 100%;
      max-height: 500px;
    }
    .container {
      flex-direction: row;
    }
    .reverse {
      flex-direction: row-reverse;
    }
    .image {
      flex: 1;
      margin-top: 0px;
      margin-right: 20px;
    }
    .text {
      flex: 2;
    }
  }
</style>

<Tile>
  <div class="container" class:reverse>
    <div class="image">
      <img src="test.jpg" alt="Image of me doing coding." />
    </div>

    <div class="text">
      {#if title}
        <h2>{title}</h2>
      {/if}
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
  </div>
</Tile>
