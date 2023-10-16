<script>
  export let product
</script>

<div class="product">
  {#each Object.entries(product) as item}
    <p>{item}</p>
  {/each}
</div>

<style>
  .product {
    background-color: yellow;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
