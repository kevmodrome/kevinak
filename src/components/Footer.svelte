<script>
  import FooterColumn from "./common/FooterColumn.svelte";
</script>

<style>
  .container {
    min-height: 370px;
    background: #202660;
    color: white;
    display: flex;
    justify-content: flex-start;
    margin: 0 auto;
    padding: 0 20px;
    padding-top: 25px;
  }

  .center {
    max-width: 1200px;
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .columns {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  h4 {
    font-family: "Merriweather";
    font-size: 28px;
    max-width: 280px;
    flex: 0 1 auto;
    margin-bottom: 20px;
  }
  @media (min-width: 500px) {
    .container {
      padding: 0 40px;
      padding-top: 60px;
    }
    .columns {
      flex-direction: row;
      justify-content: space-between;
    }
    h4 {
      max-width: 100%;
      margin-bottom: 30px;
    }
    .columns {
      flex-direction: row;
      justify-content: space-between;
    }
  }
  @media (min-width: 1080px) {
    .container {
      padding: 0 60px;
      padding-top: 80px;
      flex-direction: column;
    }
    h4 {
      max-width: 100%;
      margin-bottom: 40px;
    }
  }
</style>

<footer class="container">
  <div class="center">
    <h4>...so you’ve come to the end of the line?</h4>
    <div class="columns">
      <FooterColumn />
      <FooterColumn />
      <FooterColumn />
      <FooterColumn />
    </div>
  </div>
</footer>
