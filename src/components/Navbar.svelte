<script>
  // your script goes here
  export let title = "Lista de Canciones";
  export let clear = false;
  export let to="/";
</script>

<!-- markup (zero or more items) goes here -->

<main>
  <nav>
    <div class="nav-wrapper">
      <a href={to} class="left brand-logo">{title}</a>
      {#if clear == true } 
      <ul  class="right ">
        <li><a href="/"><i class="material-icons">clear</i></a></li>
      </ul>
      {/if}
    </div>
  </nav>
</main>

<style>
  /* your styles go here */
  nav {
    background-color: cadetblue;
    padding-left: 10px;
    overflow: hidden;
    position: fixed;
    width: 100%;
    top: 0;
  } 
  .material-icons{
    font-size: 35px;
  }
  @media only screen and (max-width: 503px) {
    .brand-logo {
      font-size: 29px;
    }
    nav{
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
      height: 10vh;
    }
  }
  @media only screen and (max-width: 430px) {
    .brand-logo {
      font-size: 26px;
      font-weight: bold;
    }
    nav{
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
    }
  }
  @media only screen and (max-width: 380px) {
    .brand-logo {
      font-size: 24px;
      font-weight: bold;
    }
  }
  @media only screen and (max-width: 346px) {
    .brand-logo {
      font-size: 23px;
      font-weight: bold;
    }
  }
  @media only screen and (max-width: 277px) {
    .brand-logo {
      font-size: 20px;
      font-weight: bolder;
    }
  }
  @media only screen and (max-width: 241px) {
    .brand-logo {
      font-size: 18px;
      font-weight: bolder;
    }
  }
  @media only screen and (max-width: 206px) {
    .brand-logo {
      font-size: 16px;
      font-weight: bolder;
    }
  }
</style>
