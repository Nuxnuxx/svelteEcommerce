<script>
  import Products from '../Components/Products.svelte'

  import SearchBar from '../Components/SearchBar.svelte'
</script>

<div class="container">
  <SearchBar />
  <Products />
</div>

<style>
  .container {
    display: grid;
    grid-template-columns: 20% 80%;
		width: 100%;
  }
</style>
