<script>
  import FooterColumn from "./common/FooterColumn.svelte";
</script>

<style>
  .container {
    min-height: 370px;
    background: #202660;
    color: white;
    display: flex;
    justify-content: center;
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
    align-items: stretch;
  }

  a {
    color: white;
    font-weight: bold;
    text-decoration: none;
    padding: 1em 0;
  }

  a:visited {
    color: whitesmoke;
  }

  ul {
    padding-left: 10px;
  }

  li {
    list-style-type: none;
    margin: 0 10px;
  }

  h4 {
    font-family: "Merriweather";
    font-size: 28px;
    max-width: 280px;
    flex: 0 1 auto;
    margin-bottom: 20px;
  }
  p {
    font-size: 14px;
  }
  @media (min-width: 500px) {
    .container {
      padding: 0 40px;
      padding-top: 60px;
    }
    .columns {
      flex-direction: row;
      justify-content: space-between;
      align-items: space-between;
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
      <FooterColumn title="Connect with me">
        <ul>
          <li>
            <a href="/">Github</a>
          </li>
          <li>
            <a href="/">LinkedIn</a>
          </li>
          <li>
            <a href="/">Instagram</a>
          </li>
          <li>
            <a href="/">Keybase</a>
          </li>
        </ul>
      </FooterColumn>
      <FooterColumn title="About This Website">
        <p>
          This website is built using Svelte and Sapper. If you want to read
          more about it you can do it
          <a href="/">here.</a>
        </p>
      </FooterColumn>
    </div>
  </div>
</footer>
