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
  }

  .selected {
    position: relative;
    display: inline-block;
  }

  .selected::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(255, 62, 0);
    display: block;
    bottom: -1px;
  }

  a {
    text-decoration: none;
    padding: 1em 0.5em;
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
