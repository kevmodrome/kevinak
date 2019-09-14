<script>
  import Image from "svelte-image";
</script>

<style>
  .background {
    box-shadow: 15px 15px 0px 0px rgba(53, 63, 153, 1);
    margin-right: 15px;
    margin-bottom: 30px;
    display: flex;
    flex-direction: column;
  }
  @media (min-width: 400px) {
    .background {
      box-shadow: 25px 25px 0px 0px rgba(53, 63, 153, 1);
      margin-right: 25px;
      margin-bottom: 50px;
      flex-direction: row;
    }
  }
  @media (min-width: 1080px) {
    .background {
      box-shadow: 35px 35px 0px 0px rgba(53, 63, 153, 1);
      margin-right: 35px;
      margin-bottom: 70px;
      flex-direction: row;
    }
  }
</style>

<div class="background">
  <slot>Missing content. Please add something to the component.</slot>
</div>
