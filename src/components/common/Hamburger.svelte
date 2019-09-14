<script>
  export let white;
  export let close;
</script>

<style>
  .white {
    filter: brightness(0) invert(1);
  }
</style>

{#if close}
  <img class:white src="close.svg" alt="Menu button" />
{:else}
  <img class:white src="hamburger.svg" alt="Menu button" />
{/if}
