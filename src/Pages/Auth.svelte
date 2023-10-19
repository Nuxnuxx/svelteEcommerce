<script>
  import Login from '../Components/Login.svelte'
  import Register from '../Components/Register.svelte'
  let bool = true
</script>

<div class="auth">
		<h1>i am palpatine</h1>
  <div class="button-wrapper">
    <button on:click={() => bool = true}>Login</button>
    <button on:click={() => bool = false}>Register</button>
  </div>

  {#if bool}
    <Login />
  {:else}
    <Register />
  {/if}
</div>
	

	<style>
		.auth {
		}
	</style>
