<script>
  import Logo from "./common/Logo.svelte";
  import Hamburger from "./common/Hamburger.svelte";
  export let segment;
  let showMobileMenu = false;
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
      height: 150px;
      justify-content: space-between;
    }
  }

  .logo-container {
    flex: 0 1 auto;
    max-width: 65px;
  }

  @media (min-width: 800px) {
    .logo-container {
      max-width: 135px;
    }
  }

  a {
    position: relative;
    color: black;
    font-weight: bold;
  }

  a:hover:before {
    right: auto;
    width: 100%;
  }

  a:before {
    content: "";
    position: absolute;
    width: 0%;
    height: 3px;
    bottom: 13px;
    left: 0;
    background-color: #353f99;
    transition: all 0.2s ease-in-out 0s;
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

  .selected {
    position: relative;
    display: inline-block;
  }

  .selected::after {
    position: absolute;
    content: "";
    width: 100%;
    height: 3px;
    background-color: #353f99;
    display: block;
  }

  a {
    text-decoration: none;
    padding: 1em 0;
    display: block;
  }

  .mobile-menu {
    position: fixed;
    background-color: #353f99;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    border-bottom-right-radius: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .menu-items {
    background: red;
  }
</style>

<nav>
  <div class="burger">
    <Hamburger />
  </div>
  <div class="logo-container">
    <Logo />
  </div>
  <ul>
    <li>
      <a class={segment === undefined ? 'selected' : ''} href=".">HOME</a>
    </li>
    <li>
      <a class={segment === 'about' ? 'selected' : ''} href="about">WORK</a>
    </li>
    <li>
      <a class={segment === undefined ? 'selected' : ''} href=".">ABOUT</a>
    </li>
    <li>
      <a
        rel="prefetch"
        class={segment === 'blog' ? 'selected' : ''}
        href="blog">
        BLOG
      </a>
    </li>
  </ul>
</nav>

{#if !showMobileMenu}
  <div class="mobile-menu">
    <div class="menu-items">Hej</div>
  </div>
{/if}
