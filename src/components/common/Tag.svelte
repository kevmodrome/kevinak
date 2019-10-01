<style>
  li {
    list-style: none;
    float: left;
  }

  .tag {
    background: #eee;
    border-radius: 3px;
    color: #999;
    display: inline-block;
    height: 26px;
    line-height: 26px;
    padding: 0 10px;
    margin: 0 10px 10px 0;
    text-decoration: none;
    transition: 200ms all;
  }

  .tag:hover {
    background: #202660;
    color: white;
  }
</style>

<li>
  <a href="/" class="tag">
    <slot />
  </a>
</li>
