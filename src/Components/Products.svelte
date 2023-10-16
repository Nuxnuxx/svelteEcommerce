<script>
  import { onMount } from 'svelte'
  import Product from './Product.svelte'
  import axios from 'axios'
  import { apiData } from '../store'

  onMount(async () => {
    try {
      let products = await axios.get('https://fakestoreapi.com/products')
			apiData.set(products.data)
    } catch (e) {
      throw new Error(e)
    }
  })
</script>

<div class="products">
  {#each $apiData as product}
    <Product {product} />
  {/each}
</div>

<style>
  .products {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    justify-items: center;
    text-align: center;
    align-content: center;
  }
</style>
