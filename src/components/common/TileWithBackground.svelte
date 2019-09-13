<script>
  import Image from "svelte-image";
</script>

<style>
  .background {
    box-shadow: 15px 15px 0px 0px rgba(53, 63, 153, 1);
    display: flex;
  }
  @media (min-width: 400px) {
    .background {
      box-shadow: 35px 35px 0px 0px rgba(53, 63, 153, 1);
    }
  }
  @media (min-width: 1080px) {
    .background {
      box-shadow: 50px 50px 0px 0px rgba(53, 63, 153, 1);
    }
  }
</style>

<div class="background">
  <slot>Missing content. Please add something to the component.</slot>
</div>
