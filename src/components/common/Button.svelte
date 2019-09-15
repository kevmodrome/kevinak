<script>
  export let outline;
  export let primaryOutline;
  export let blackOutline;
</script>

<style>
  button {
    position: relative;
    padding: 10px 15px;
    color: white;
    font-weight: bold;
    font-size: 14px;
    background: #353f99;
    border-radius: 8px;
    border: none;
    transition: outline 0.6s linear;
  }
  .outline {
    background: transparent;
  }
  .outline:after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    border: solid 3px white;
    border-radius: 8px;
    z-index: -1;
  }
  .primaryOutline {
    background: transparent;
    color: #353f99;
    border: solid 3px #353f99;
    border-radius: 8px;
  }
  .primaryOutline {
    color: black;
    border: solid 3px black;
  }
  .blackOutline {
    background: transparent;
    color: black;
    border: solid 3px black;
    border-radius: 8px;
  }
  .blackOutline:hover {
    color: #353f99;
    border: solid 3px #353f99;
  }
</style>

<button class:outline class:primaryOutline class:blackOutline>
  <slot />
</button>
