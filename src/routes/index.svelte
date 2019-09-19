<script>
  import Divider from "../components/common/Divider.svelte";

  import Headline from "../components/home/Headline.svelte";
  import About from "../components/home/About.svelte";
  import Work from "../components/home/Work.svelte";
  import Skills from "../components/home/Skills.svelte";
</script>

<style>
  div {
    margin-bottom: 100px;
    margin: 0 auto;
  }
</style>

<svelte:head>
  <title>Kevin Åberg Kultalahti's Personal Website</title>
</svelte:head>

<div>
  <Headline />
  <Divider />
  <About />
  <Divider />
  <Work />
  <Divider />
  <Skills />
</div>
