<script>
  import Tile from "../common/Tile.svelte";
  import Client from "../home/Client.svelte";
</script>

<style>
  div {
    margin-top: 20px;
    display: flex;
    justify-content: flex-end;
  }

  a {
    position: relative;
    font-weight: bold;
    text-decoration: none;
    padding: 1em 0;
    display: block;
  }

  a:hover:before {
    right: auto;
    width: 100%;
  }

  a:visited {
    color: black;
  }

  a:before {
    content: "";
    position: absolute;
    width: 0%;
    height: 3px;
    bottom: 20px;
    left: 0;
    background-color: #353f99;
    transition: all 0.2s ease-in-out 0s;
  }
</style>

<Tile>
  <h2>Work</h2>
  <Client />
  <Client />
  <div>
    <a href="/">
      <h3>See more of my work &#8594</h3>
    </a>
  </div>
</Tile>
