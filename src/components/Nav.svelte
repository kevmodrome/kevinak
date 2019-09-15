<script>
  import { fade } from "svelte/transition";
  import Logo from "./common/Logo.svelte";
  import Hamburger from "./common/Hamburger.svelte";
  import MenuItem from "./common/MenuItem.svelte";
  import FullScreenMenu from "./FullScreenMenu.svelte";
  export let segment;
  let visible = false;

  const setVisible = () => {
    visible = !visible;
  };
</script>

<style>
  nav {
    width: 100%;
    height: 100px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  @media (min-width: 500px) {
    nav {
      height: 120px;
      justify-content: space-between;
    }
  }

  .logo-container {
    flex: 0 1 auto;
    max-width: 65px;
  }

  @media (min-width: 800px) {
    .logo-container {
      max-width: 100px;
    }
  }

  ul {
    display: none;
  }
  @media (min-width: 500px) {
    ul {
      display: flex;
      flex: 1 1 auto;
      margin: 0;
      padding: 0;
      justify-content: flex-end;
    }
  }
  ul::after {
    content: "";
    display: block;
  }

  li {
    display: block;
    padding: 0 1em;
  }

  .burger {
    display: initial;
    position: absolute;
    top: 20px;
    left: 20px;
  }

  @media (min-width: 500px) {
    .burger {
      display: none;
    }
  }
</style>

<FullScreenMenu {visible} {setVisible} {segment} />

<nav>
  {#if !visible}
    <div class="burger" on:click={setVisible} transition:fade>
      <Hamburger />
    </div>
  {/if}
  <div class="logo-container">
    <Logo />
  </div>
  <ul>
    <li>
      <MenuItem active={segment === undefined} href=".">HOME</MenuItem>
    </li>
    <li>
      <MenuItem active={segment === 'work'} href="work">WORK</MenuItem>
    </li>
    <li>
      <MenuItem active={segment === 'about'} href="about">ABOUT</MenuItem>
    </li>
    <li>
      <MenuItem prefetch active={segment === 'blog'} href="blog">BLOG</MenuItem>
    </li>
  </ul>
</nav>
