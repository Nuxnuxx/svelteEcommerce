<script>
  import { Link } from 'svelte-routing'
</script>

<nav>
  <Link to="/">Home</Link>
  <Link to="/about">About</Link>
  <Link to="/shop">Shop</Link>
  <Link to="/cart">Cart</Link>
  <Link to="/register">Register / Login</Link>
</nav>

<style>
  nav {
    width: 100%;
    height: 5rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 2rem;
  }
</style>
