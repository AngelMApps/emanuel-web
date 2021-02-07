<script>
  // your script goes here
  import Footer from "../components/Footer.svelte";
  let imgURL1="https://scontent.flim18-2.fna.fbcdn.net/v/t1.0-9/144931676_3587007431425336_2334257498386606311_o.jpg?_nc_cat=111&ccb=2&_nc_sid=730e14&_nc_eui2=AeEjRSIeLEU7GzF0Z0t3svTR5bqMAHTgizXluowAdOCLNfwY6d869GacwhhGxxdzoZHT2h8nASu6UInIj-xM1Ljv&_nc_ohc=SflW2rHDjvEAX-NXZ9u&_nc_ht=scontent.flim18-2.fna&oh=6b967420d5e81bc6b5084d38dcc9fc21&oe=6043F2A3";
  let fondo2 ="https://i.ibb.co/gZq6Wzx/to-the-new-year-3.png";
</script>

<!-- markup (zero or more items) goes here -->
<main>
  <div class="container-div">
    <div class="parallax-container">
      
      <div class="parallax"><img alt="fondo" src={imgURL1}></div>
    </div>
    <div class="section teal darken-4">
      <div class="row container center">
        <h2 class="header white-text">Iglesia Misión Cristiana Emanuel</h2>
        <h3 class="white-text">"Dios con Nosotros"</h3>
        <strong class="grey-text text-lighten-4">Dios te trajo y Nosotros te recibimos con amor.</strong>
      </div>
    </div>
    <div class="parallax-container">
      <div class="parallax"><img alt="fondo" src={fondo2}></div>
    </div>
    <Footer />
  </div>
</main>

<style>
  /* your styles go here */
  strong{
    font-size: 26px;
  }
  .container-div {
    display: flex;
    flex-direction: column;
  }
  

</style>
