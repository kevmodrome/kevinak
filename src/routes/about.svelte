<script>
  import Divider from "../components/common/Divider.svelte";

  import Headline from "../components/home/Headline.svelte";
  import About from "../components/home/About.svelte";
  import Work from "../components/home/Work.svelte";
  import Skills from "../components/home/Skills.svelte";
  import Instagram from "../components/home/Instagram.svelte";
  import Footer from "../components/Footer.svelte";
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
  <Headline />
  <Divider />
  <About />
  <Divider />
  <Work />
  <Divider />
  <Skills />
  <Divider />
  <Instagram />
</div>
