<script>
  import { Link } from 'svelte-routing'
</script>

<header>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/shop">Shop</Link>
    <Link to="/cart">Cart</Link>
    <Link to="/auth">Register / Login</Link>
  </nav>
</header>

<style>
  nav {
    width: 100%;
    height: 5rem;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    font-size: 1.5rem;
  }
</style>
