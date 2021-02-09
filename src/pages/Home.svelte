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
        <!--Cards-->
        <div class="row">
          <div class="col s12 m6 l6">
            <div class="card z-depth-4">
              <div class="card-content">
                <span class="card-title">Card Title</span>
                <ul>
                  <span class="text-past">Neil Angel Mora Sanchez</span>
                  <br />
                  <span class="text-past">Susi Santos Huamanchay Leiva</span>
                </ul>
              </div>
            </div>
          </div>
          <div class="col s12 m6 l6">
            <div class="card z-depth-4">
              <div class="card-content">
                <span class="card-title">Dirección:</span>
                <a
                  class="link-map"
                  target="_blank"
                  href="https://goo.gl/maps/NjvUGU6VUwqEjr3W8"
                  >Sect-3 Grp23-A Mz-H Lt-14<br />
                  <i class="fas fa-map-marked-alt" /></a
                >
              </div>
            </div>
          </div>
        </div>

        <div class="row">
          <div class="col s12 m6 l5">
            <div class="card z-depth-4">
              <div class="card-content">
                <span class="card-title">Visión:</span>
                <p>Ganar, Consolidar, Discipular y Enviar</p>
              </div>
            </div>
          </div>
          <div class="col s12 m6 l7">
            <div class="card z-depth-4">
              <div class="card-content">
                <span class="card-title">Misión:</span>
                <p>Ganar la gran comisión a través de los Grupos Familiares</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <Footer />
    </div>
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
  p {
    font-size: 18px;
  }
  img {
    height: 150px;
  }
  .fa-map-marked-alt {
    font-size: 35px;
  }
  .link-map {
    color: black;
    font-size: 20px;
  }
  .link-map:hover {
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
  @media only screen and (max-width: 762px) {
    .text-past {
      font-size: 16px;
      font-weight: 300;
    }
    p {
      font-size: 16px;
    }
    .link-map {
      font-size: 17px;
    }
  }
  @media only screen and (max-width: 631px) {
    .black-text {
      font-size: 46px;
    }
  }
  @media only screen and (max-width: 511px) {
    .black-text {
      font-size: 48px;
    }
    .image-div {
      animation: App-logo-spin infinite 30s linear;
    }
    .img-style{
      height: 300px;
    }
    .row-div {
      display: flex;
      flex-direction: column-reverse;
    }
  }
  
@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
  @media only screen and (max-width: 420px) {
    .header{
      font-size: 35px;
    }
    .black-text{
      font-size: 40px;
    }
  }
  @media only screen and (max-width: 420px) {
    .header{
      font-size: 35px;
    }
    .black-text{
      font-size: 40px;
    }
    .img-style{
      height: 200px;
    }
  }
  @media only screen and (max-width: 320px) {
    .header{
      font-size: 35px;
    }
    .black-text{
      font-size: 32px;
    }
    .img-style{
      height: 150px;
    }
  }
  @media only screen and (max-width: 240px) {
    .header{
      font-size: 30px;
    }
    .black-text{
      font-size: 27px;
    }
    .img-style{
      height: 150px;
    }
  }
</style>
