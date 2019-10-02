<script>
  import FooterColumn from "./common/FooterColumn.svelte";
</script>

<style>
  .container {
    background: #202660;
    color: white;
    display: flex;
    justify-content: center;
    margin: 0 auto;
    padding: 30px 20px;
  }

  .center {
    max-width: 1200px;
    width: 100%;
  }
  .columns {
    margin: 20px auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-column-gap: 10px;
    grid-row-gap: 10px;
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
  p {
    font-size: 14px;
  }
  @media (min-width: 500px) {
    .container {
      padding: 40px;
    }
  }
  @media (min-width: 1080px) {
    .container {
      padding: 60px;
    }
  }
</style>

<footer class="container">
  <div class="center">
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
      <FooterColumn title="Sitemap">
        <ul>
          <li>
            <a href="/">Home</a>
          </li>
          <li>
            <a href="/">Work</a>
          </li>
          <li>
            <a href="/">About</a>
          </li>
          <li>
            <a href="/">Blog</a>
          </li>
          <li>
            <a href="/">Reach Out</a>
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
