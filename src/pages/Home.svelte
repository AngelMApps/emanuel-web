<script>
  // your script goes here

import Fondo from "../components/Fondo.svelte";
import Footer from "../components/Footer.svelte";

 
</script>

<!-- markup (zero or more items) goes here -->
<main>
 <div class="container-div">
  <Fondo/>
  <Footer/>
 </div>
</main>

<style>
  /* your styles go here */
  .container-div{
    display: flex;
    flex-direction: column;
  }
  
</style>
