<script>
  // your script goes here
  import Footer from "../components/Footer.svelte";
</script>

<!-- markup (zero or more items) goes here -->
<main>
  <div class="container-div">
    <div class="row-div">
      <div class="image-div">
        <img alt="icono" src="assets/img/icono.png" class="img-style" />
      </div>
      <div class="title-div"><h1 class="black-text">Iglesia Emanuel</h1></div>
    </div>
    <div class="section">
      <div class="row container center">
        <h2 class="header">Fundada el 8 de octubre de 1990</h2>
        <!--Card Pastores-->
        <div class="col s12 m6 l4">
          <div class="card z-depth-4">
            <strong class="card-title">Pastores:</strong>
            <hr />
            <ul>
              <span class="text-past">Neil Angel Mora Sanchez</span>
              <br />
              <span class="text-past">Susi Santos Huamanchay Leiva</span>
            </ul>
          </div>
        </div>
        <div class="col s12 m6 l4">
          <div class="card z-depth-4">
            <strong class="card-title">Dirección:</strong>
            <hr />
            <a class="link-map" target="_blank" href="https://goo.gl/maps/NjvUGU6VUwqEjr3W8"
              >Sect-3 Grp23-A Mz-H Lt-14<br />
              <i class="fas fa-map-marked-alt" /></a
            >
          </div>
        </div>

      </div>
    </div>
    <Footer />
  </div>
</main>

<!-- markup (zero or more items) goes here -->
<style>
  /* your styles go here */
  /*strong{
    font-size: 26px;
  }*/
  .container-div {
    display: flex;
    flex-direction: column;
  }
  .text-past {
    font-size: 19px;
    font-weight: 300;
  }
  img {
    height: 150px;
  }
  .fa-map-marked-alt {
    font-size: 30px;
  }
  .link-map{
    color: black;
  }
  .link-map:hover{
    color: cadetblue;
  }
  a {
    font-size: 20px;
  }
  h1 {
    font-weight: 500;
  }
  .card-title {
    font-weight: bold;
  }
  .row-div {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
</style>
