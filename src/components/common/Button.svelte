<script>
  export let outline;
  export let primaryOutline;
  export let blackOutline;
</script>

<style>
  button {
    padding: 10px 15px;
    color: white;
    background: #353f99;
    font-size: 24px;
    border-radius: 8px;
  }
  .outline {
    background: transparent;
    border: 2px solid white;
  }
  .primaryOutline {
    background: transparent;
    color: #353f99;
    border: 1px solid #353f99;
  }
  .blackOutline {
    background: transparent;
    color: black;
    border: 1px solid black;
  }
</style>

<button class:outline class:primaryOutline class:blackOutline>
  <slot />
</button>
