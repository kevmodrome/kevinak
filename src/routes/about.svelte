<script>
  import Divider from "../components/common/Divider.svelte";
  import Headline from "../components/common/Headline.svelte";
  import About from "../components/common/About.svelte";
  import GoodAt from "../components/about/GoodAt.svelte";
  import Projects from "../components/about/Projects.svelte";
</script>

<style>
  div {
    margin-bottom: 100px;
    margin: 0 auto;
  }
</style>

<svelte:head>
  <title>Kevin Åberg Kultalahti's Personal Website - About</title>
</svelte:head>

<div>
  <Headline title="About Me" />
  <About reverse />
  <Divider />
  <GoodAt title="What I'm Good At" />
  <Divider />
  <Projects />
</div>
