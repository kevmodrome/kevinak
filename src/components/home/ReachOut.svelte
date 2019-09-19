<script>
  import Button from "../common/Button.svelte";
</script>

<style>
  div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    align-content: flex-start;
  }

  h2 {
    color: black;
    font-size: 48px;
    text-align: center;
    margin: 0;
  }

  p {
    text-align: center;
    max-width: 320px;
  }
</style>

<div>
  <h2>Reach Out</h2>
  <p>
    Are you looking for someone to efficiently and swiftly create your next
    project? Reach out by clicking the button bellow.
  </p>
  <Button big>CONTACT</Button>
</div>
