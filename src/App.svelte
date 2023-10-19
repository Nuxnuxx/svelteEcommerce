<script>
  import { Route, Router } from 'svelte-routing'
  import Home from './Pages/Home.svelte'
  import Header from './Components/Header.svelte'
  import About from './Pages/About.svelte'
  import Shop from './Pages/Shop.svelte'
  import Cart from './Pages/Cart.svelte'
  import Footer from './Components/Footer.svelte'

  import './styles.css'
  import Auth from './Pages/Auth.svelte'

  export let url = ''
</script>

<Router {url}>
  <Header />
  <div>
    <Route path="/" component="{Home}"></Route>
    <Route path="/about" component="{About}"></Route>
    <Route path="/shop" component="{Shop}"></Route>
    <Route path="/cart" component="{Cart}"></Route>
    <Route path="/auth" component="{Auth}"></Route>
  </div>
  <Footer />
</Router>
