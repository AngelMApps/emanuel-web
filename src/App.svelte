<script>
  import {Router, Route} from "svelte-routing";
  import Navbar from "./components/Navbar.svelte";
  import DetailPageSongs from "./pages/Detail_songs.svelte";
  import Songs from "./pages/Songs.svelte";
  import Home from './pages/Home.svelte';
  import Cultos from "./pages/Cultos.svelte";
  import DetailPageCulto from './pages/Detail_cultos.svelte';
  import Devocional from "./pages/Devocional.svelte";
  import DetailDevocional from "./pages/Detail_devocional.svelte";
</script>

<main>
  <Router>
    <div>
      <Route path="/">
        <Navbar />
        <Home />
      </Route>

      <!--rutas de cultos-->
      <Route path="/cultos">
        <Navbar />
        <Cultos />
      </Route>
      <Route  path="/culto/:id/:dia" let:params>
        <Navbar />
        <DetailPageCulto id={params.id} />
      </Route>

      <!--rutas de devocionales-->
      <Route path="/devocionales">
        <Navbar/>
        <Devocional />
      </Route>
      <Route path="/devocional/:id" let:params>
        <Navbar/>
        <DetailDevocional id={params.id} />
      </Route>

      <!--rutas de Canciones-->
      <Route path="/canciones">
        <Navbar />
        <Songs />
      </Route>
      <Route path="/detail/:id/:dia" let:params>
        <Navbar />
        <DetailPageSongs dia ={params.dia} />
      </Route>
    </div>
  </Router>
</main>
