<script>
  import { Router, Route } from "svelte-routing";
  import Navbar from "./components/Navbar.svelte";
  import DetailPage from "./pages/Detail.svelte";
  import Home from "./pages/Home.svelte";
</script>

<main>
  <Router>
    <div>
      <Route path="/">
        <Navbar />
        <Home />
      </Route>
      <Route path="/detail/:id/:dia" let:params>
        <Navbar title={params.dia} to={`/detail/${params.id}/${params.dia}`} clear={true} />
        <DetailPage  dia ={params.dia} />
      </Route>
    </div>
  </Router>
</main>
