<script>
  import Tile from "../common/Tile.svelte";
  import ReachOut from "./ReachOut.svelte";
  import SkillsBox from "../common/SkillsBox.svelte";
</script>

<style>
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-column-gap: 20px;
    grid-row-gap: 20px;
    align-items: center;
  }
  .skills {
    display: none;
  }
  @media (min-width: 800px) {
    .skills {
      display: initial;
    }
  }
</style>

<Tile>
  <div class="container">
    <div class="call-to-action">
      <ReachOut />
    </div>
    <div class="skills">
      <SkillsBox />
    </div>
  </div>
</Tile>
