<div class="search-bar">
  <input type="text" />
  <div class="category">
    <p>HIKING</p>
    <p>SKIING</p>
    <p>RUNNING</p>
    <p>BASKETBALL</p>
    <p>FOOTBALL</p>
    <p>SURF</p>
  </div>
</div>

<style>
  .search-bar {
    display: flex;
    flex-direction: column;
    background-color: #666;
    padding: 2rem;
    row-gap: 1rem;
  }
  .category {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    row-gap: 1rem;
  }
</style>
