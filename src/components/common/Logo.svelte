<script>
  export let white;
</script>

<style>
  img {
    width: 100%;
  }
</style>

{#if white}
  <img src="logo_white.svg" alt="KÅK logotype" />
{:else}
  <img src="logo.svg" alt="KÅK logotype" />
{/if}
