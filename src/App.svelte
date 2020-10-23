<script>
  // import pages
  import Home from './pages/Home.svelte'
  import About from './pages/About.svelte'
  import Products from './pages/Products.svelte'
  import ProductTemplate from './pages/ProductTemplate.svelte'
  import Checkout from './pages/Checkout.svelte'
  import Login from './pages/Login.svelte'
  // router
  import { Router, Link, Route } from 'svelte-routing'
</script>

<Router>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/products">Products</Link>
  </nav>
  <div>
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
    <Route path="/login" component={Login} />
    <Route path="/products" component={Products} />
    <Route path="/products/:id" component={ProductTemplate} />
  </div>
</Router>
