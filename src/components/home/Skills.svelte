<script>
  import Tile from "../common/Tile.svelte";
  import ReachOut from "./ReachOut.svelte";
  import SkillsBox from "../common/SkillsBox.svelte";
</script>

<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .call-to-action {
    flex: 1 1 0;
  }
  .skills {
    flex: 1 1 0;
    display: none;
  }
  @media (min-width: 500px) {
    .container {
      justify-content: center;
    }
    .skills {
      display: none;
    }
  }
  @media (min-width: 1080px) {
    .container {
      justify-content: space-between;
    }
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
