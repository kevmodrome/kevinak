<script>
  export let outline;
  export let primaryOutline;
  export let blackOutline;
  export let big;
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
    transition: all 0.2s linear;
    cursor: pointer;
  }
  button:hover {
    background: #202660;
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
  .primaryOutline:hover {
    background: #353f99;
    color: white;
    border-radius: 8px;
  }
  .blackOutline {
    background: transparent;
    color: black;
    border: solid 3px black;
    border-radius: 8px;
  }
  .blackOutline:hover {
    background: transparent;
    color: #353f99;
    border: solid 3px #353f99;
  }
  .big {
    padding: 15px 20px;
    font-size: 18px;
  }
</style>

<button class:outline class:primaryOutline class:blackOutline class:big>
  <slot />
</button>
