<script>
  import { fly, fade } from "svelte/transition";
  import Hamburger from "./common/Hamburger.svelte";
  import Logo from "./common/Logo.svelte";
  import MenuItem from "./common/MenuItem.svelte";
  export let visible;
  export let setVisible;
  export let segment;
</script>

<style>
  .logo-container {
    max-width: 135px;
  }
  ul {
    padding-inline-start: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  ul::after {
    content: "";
    display: block;
  }

  li {
    display: block;
  }
  .close-button {
    position: fixed;
    top: 20px;
    left: 20px;
    z-index: 101;
  }

  .mobile-menu {
    position: fixed;
    background-color: #353f99;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    border-bottom-right-radius: 1000px;
    z-index: 100;
  }

  .menu-items {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 101;
  }
</style>

{#if visible}
  <div
    class="mobile-menu"
    in:fly={{ y: -2000, x: -1000, duration: 1000, opacity: 1 }}
    out:fly={{ y: -2000, x: -1000, delay: 300, duration: 1000, opacity: 1 }} />
  <div
    class="menu-items"
    in:fade={{ delay: 500, duration: 300 }}
    out:fade={{ delay: 0, duration: 300 }}>
    <div class="logo-container">
      <Logo white />
    </div>
    <ul on:click={setVisible}>
      <li in:fly={{ y: -20, delay: 500, duration: 1000 }}>
        <MenuItem white active={segment === undefined} href=".">HOME</MenuItem>
      </li>
      <li in:fly={{ y: -20, delay: 600, duration: 1000 }}>
        <MenuItem white active={segment === 'work'} href="work">WORK</MenuItem>
      </li>
      <li in:fly={{ y: -20, delay: 700, duration: 1000 }}>
        <MenuItem white active={segment === 'about'} href="about">
          ABOUT
        </MenuItem>
      </li>
      <li in:fly={{ y: -20, delay: 800, duration: 1000 }}>
        <MenuItem white prefetch active={segment === 'blog'} href="blog">
          BLOG
        </MenuItem>
      </li>
    </ul>
  </div>
  <div
    in:fade={{ delay: 500, duration: 300 }}
    out:fade={{ delay: 0, duration: 150 }}
    class="close-button"
    on:click={setVisible}>
    <Hamburger close />
  </div>
{/if}
