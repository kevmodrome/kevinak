<script>
  export let white;
</script>

<style>

</style>

{#if white}
  <img src="hamburger_white.svg" alt="Menu button" />
{:else}
  <img src="hamburger.svg" alt="Menu button" />
{/if}
