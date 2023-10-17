<script lang="ts">
  import { onMount } from 'svelte'
  import axios from 'axios'
  import { apiData } from '../store'
  let categories: [] = []

  onMount(async () => {
    try {
      const response = await axios.get(
        'https://fakestoreapi.com/products/categories',
      )
      categories = response.data
    } catch (e) {
      throw new Error(e)
    }
  })

  const handleClick = async (event: HTMLElement) => {
    try {
      const response = await axios.get(`https://fakestoreapi.com/products/category/${event.target.textContent}`)
			console.log(response.data)
			apiData.set(response.data)
    } catch (e) {
      throw new Error(e)
    }
  }
</script>

<div class="search-bar">
  <input type="text" />
  <div class="category">
    {#each categories as categorie}
      <div on:click={handleClick}>{categorie}</div>
    {/each}
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
