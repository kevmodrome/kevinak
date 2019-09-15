<style>
  .container {
    display: flex;
    flex-direction: column;
  }
  .text {
    flex: 1;
    margin-right: 0;
    margin-bottom: 10px;
  }
  .title {
    margin-bottom: 10px;
  }
  .image {
    flex: 1;
  }
  img {
    width: 100%;
    max-height: 150px;
    object-fit: cover;
  }
  @media (min-width: 500px) {
    .container {
      flex-direction: row;
    }
    .text {
      flex: 3;
      margin-right: 20px;
      margin-bottom: 0;
    }
    .image {
      flex: 1;
    }
  }
  @media (min-width: 1080px) {
    .container {
      flex-direction: row;
    }
    .text {
      flex: 3;
      margin-right: 20px;
      margin-bottom: 0;
    }
    .image {
      flex: 1;
    }
  }
</style>

<div class="container">
  <div class="text">
    <h3 class="title">Mäklarsamfundets Kundvägledarna</h3>
    <div class="text">
      Mäklarsamfundet wanted a website for their new service
      <span>
        <a href=".">Kundvägledarna</a>
      </span>
      . The idea in short is about helping real estate buyers and sellers by
      offering a plethora of frequently asked questions as well a chat
      functionality where related questions can be asked.
    </div>
  </div>
  <div class="image">
    <img src="test.jpg" alt="Mäklarsamfundet Placeholder" />
  </div>
</div>
