<script>
  import Divider from "../components/common/Divider.svelte";

  import Headline from "../components/common/Headline.svelte";
  import About from "../components/common/About.svelte";
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
  <title>Kevin Åberg Kultalahti's Personal Website</title>
</svelte:head>

<div>
  <Headline
    image
    title="Hello, I’m Kevin, a React Native developer based in Stockholm,
    Sweden." />
  <Divider />
  <About title="About Me" />
  <Divider />
  <Work />
  <Divider />
  <Skills />
  <Divider />
  <Instagram />
</div>
