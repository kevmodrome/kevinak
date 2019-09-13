<script>
  import Image from "svelte-image";
  export let segment;
</script>

<style>
  nav {
    width: 100%;
    height: 150px;

    display: flex;
    align-items: center;
  }

  .logo-container {
    flex: 0 1 auto;
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
    flex: 1 1 auto;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: flex-end;
  }
  ul::after {
    content: "";
    display: block;
  }

  li {
    display: block;
    padding: 0 1em;
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
</style>

<nav>
  <div class="logo-container">
    <img src="logo.svg" alt="KÅK logotype" />
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
