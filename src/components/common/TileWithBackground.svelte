<script>
  import Image from "svelte-image";
</script>

<style>
  .background {
    box-shadow: 50px 50px 0px 0px rgba(53, 63, 153, 1);
    display: flex;
  }
</style>

<div class="background">
  <slot>Missing content. Please add something to the component.</slot>
</div>
