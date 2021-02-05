<script>
  // your script goes here
</script>

<!-- markup (zero or more items) goes here -->
<main>
  <footer class="page-footer">
    <div class="container">
      <div class="row">
        <div class="col l6 s12">
          <h5 class="white-text center">Contáctos</h5>
          <ul class="center">
            <li class="numbers-text">
              <a href="tel:984135388">
                <i class="fas fa-phone-alt" />
                984135388
              </a>
            </li>
            <li class="numbers-text">
              <a href="tel:951813282">
                <i class="fas fa-phone-alt" />
                951813282
              </a>
            </li>
          </ul>
        </div>
        <div class="col l4 offset-l2 s12">
          <h5 class="white-text center">Links</h5>
          <ul class="center ul-style">
            <li>
              <a
                class="grey-text text-lighten-3"
                target="_blank"
                href="https://www.facebook.com/iglesia.misioncristianaemanuel"
              >
                <div class="div-links">
                  <i class="fab fa-facebook" />
                  <span>Facebook</span>
                </div>
              </a>
            </li>
            <li>
              <a
                class="grey-text text-lighten-3"
                target="_blank"
                href="https://www.instagram.com/iglesiaemanuelof/"
              >
                <div class="div-links">
                  <i class="fab fa-instagram" />
                  <span>Instagram</span>
                </div>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      <div class="container">
        © 2021 Iglesia Emanuel
        <span class="grey-text text-lighten-4 right"
          >Bendiciones!!!</span
        >
      </div>
    </div>
  </footer>
</main>

<style>
  /* your styles go here */
  .page-footer {
    background-color: rgb(36, 67, 68);
  }
  .footer-copyright {
    background-color: rgb(29, 48, 49);
  }
  .ul-style {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
  .div-links {
    display: flex;
    flex-direction: column;
  }
  .div-links:hover {
    display: flex;
    flex-direction: column-reverse;
    color: cadetblue;
  }

  .fa-phone-alt {
    margin-right: 4px;
    font-size: 20px;
    padding-bottom: 15px;
  }
  .fa-instagram {
    font-size: 30px;
    color: rgb(255, 254, 254);
  }
  .fa-facebook {
    font-size: 30px;
    color: rgb(255, 233, 233);
  }
  .numbers-text a {
    font-size: 20px;
    color: white;
  }
  .numbers-text a:hover {
    font-size: 20px;
    color: cadetblue;
  }
  .white-text {
    font-size: 50px;
  }
  @media only screen and (max-width: 273px){
      .white-text{
          font-size: 43px;
      }
  }
  @media only screen and (max-width: 267px){
      .text-lighten-4{
          display: none;
      }
  }
</style>
