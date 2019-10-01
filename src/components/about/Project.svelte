<script>
  import Tag from "../common/Tag.svelte";
</script>

<style>
  .item {
    display: grid;
    grid-template-columns: 1fr;
  }

  img {
    width: 100%;
    height: 100%;
    max-height: 250px;
    object-fit: cover;
    padding: 0;
  }

  h3 {
    font-family: "Open Sans";
    font-style: normal;
    color: #353f99;
    margin: 0;
    font-weight: bold;
    font-size: 20px;
  }

  ul {
    list-style: none;
    margin: 0;
    overflow: hidden;
    padding: 0;
  }
</style>

<div class="item">
  <a href="/about">
    <img src="test.jpg" alt="Cool instagram pic." />
    <h3>Personal Site</h3>
    <ul>
      <Tag>HTML</Tag>
      <Tag>CSS</Tag>
      <Tag>UX</Tag>
    </ul>
  </a>
</div>
