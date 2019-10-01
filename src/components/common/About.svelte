<script>
  export let title;
  export let reverse;
  import Tile from "../common/Tile.svelte";
</script>

<style>
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-column-gap: 20px;
    max-width: 800px;
  }
  img {
    width: 100%;
    max-height: 500px;
    object-fit: cover;
  }
</style>

<Tile>
  <div class="container">
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
