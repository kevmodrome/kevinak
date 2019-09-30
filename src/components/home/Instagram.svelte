<style>
  .container {
    margin: 20px auto;
    margin-bottom: 40px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 1fr;
    grid-column-gap: 20px;
    grid-row-gap: 20px;
  }
  .grid::before {
    content: "";
    width: 0;
    padding-bottom: 100%;
    grid-row: 1 / 1;
    grid-column: 1 / 1;
  }

  .grid > *:first-child {
    grid-row: 1 / 1;
    grid-column: 1 / 1;
  }

  .item {
    background: green;
    position: relative;
  }

  .grid > * {
    box-shadow: 0 2px 30px rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    padding: 2rem 1rem;
    cursor: pointer;

    pointer-events: auto;
    transition: 300ms opacity, 300ms transform;
  }

  .grid:hover > * {
    opacity: 0.4;
  }

  .grid:hover > *:hover {
    transform: scale(1.05);
    opacity: 1;
  }

  img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    padding: 0;
  }

  h2 {
    margin-bottom: 30px;
    margin-left: 20px;
  }

  @media (min-width: 600px) {
    .container {
      margin: 50px auto;
      margin-bottom: 60px;
    }
    .grid {
      grid-template-columns: 1fr 1fr 1fr 1fr;
    }
  }
  @media (min-width: 1080) {
    .container {
      margin: 80px auto;
      margin-bottom: 60px;
    }
    .grid {
      grid-template-columns: 1fr 1fr 1fr 1fr;
    }
  }
</style>

<div class="container">
  <h2>My Tech Travels</h2>
  <div class="grid">
    <div class="item">
      <img src="test.jpg" alt="Cool instagram pic." />
    </div>
    <div class="item">
      <img src="test.jpg" alt="Cool instagram pic." />
    </div>
    <div class="item">
      <img src="test.jpg" alt="Cool instagram pic." />
    </div>
    <div class="item">
      <img src="test.jpg" alt="Cool instagram pic." />
    </div>
  </div>
</div>
