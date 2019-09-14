<script>
  export let active;
  export let text;
  export let href;
  export let prefetch;
  export let white;
</script>

<style>
  a {
    position: relative;
    color: black;
    font-weight: bold;
    text-decoration: none;
    padding: 1em 0;
    display: block;
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

  .active::after {
    position: absolute;
    content: "";
    width: 100%;
    height: 3px;
    background-color: #353f99;
    display: block;
  }

  .white {
    color: white;
  }

  .white:before {
    background-color: white;
  }

  .white-active::after {
    background-color: white;
  }
</style>

<a class:active class:white rel={prefetch ? 'prefetch' : null} {href}>
  <slot>Missing Link Text</slot>
</a>
