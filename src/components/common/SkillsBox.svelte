<script>
  import TileWithBackground from "../common/TileWithBackground.svelte";
</script>

<style>
  .container {
    padding: 20px 40px;
    width: 100%;
    background: white;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  }

  .more {
    text-align: right;
  }
  ul {
    padding-left: 30px;
  }

  li {
    list-style-type: none;
  }

  li:before {
    content: "\2713";
    color: #353f99;
    font-weight: bold;
    display: inline-block;
    width: 1.5em;
    margin-left: -1em;
  }
</style>

<TileWithBackground>
  <div class="container">
    <h3>Skills</h3>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>Javascript</li>
      <br />
      <li>React</li>
      <li>React Native</li>
      <li>Gatsby</li>
      <li>Next.js</li>
      <li>Styled Components (CSS-in-JS)</li>
      <br />
      <li>Vue</li>
      <li>Svelte</li>
      <li>Sapper</li>
    </ul>
    <div class="more">
      <a href="/">... and much more &#8594</a>
    </div>
  </div>
</TileWithBackground>
