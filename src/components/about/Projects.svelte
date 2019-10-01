<script>
  import Project from "./Project.svelte";
  import Button from "../common/Button.svelte";
</script>

<style>
  .grid {
    margin: 20px auto;
    margin-bottom: 40px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-column-gap: 25px;
    grid-row-gap: 25px;
  }

  .grid > * {
    cursor: pointer;
  }

  h2 {
    width: 100%;
    max-width: 800px;
    grid-column: 1 / -1;
    cursor: pointer;
    place-self: center;
  }

  .more {
    place-self: center;
    grid-column: 1 / -1;
  }

  a:hover {
    color: white;
  }

  @media (min-width: 600px) {
    .grid {
      margin: 50px auto;
      margin-bottom: 60px;
    }
  }
  @media (min-width: 1080) {
    .grid {
      margin: 80px auto;
      margin-bottom: 60px;
    }
  }
</style>

<div class="grid">
  <h2>Things I Built</h2>
  <Project />
  <Project />
  <Project />
  <Project />
  <Project />
  <Project />
  <div class="more">
    <a href="/work">
      <Button primaryOutline big>SEE MORE</Button>
    </a>
  </div>
</div>
