<script>
  export let title;
</script>

<style>
  .container {
    margin: 10px;
    flex: 1 1 0;
  }
  @media (min-width: 500px) {
    .container {
    }
  }
  @media (min-width: 1080px) {
    .container {
    }
  }
</style>

<div class="container">
  <h5>{title}</h5>
  <slot />
</div>
