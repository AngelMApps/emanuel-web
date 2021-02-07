<script>
  // your script goes here
  import { Link } from "svelte-routing";
  let rNav = false;
  function navbarResponsive() {
    rNav = !rNav;
    console.log(rNav);
  }
  let routes = [
    { name: "Cultos", route: "/cultos" },
    {name:"Devocionales", route:"/devocionales"},
    {name:"Canciones", route: "/canciones"},
  ];
</script>

<!-- markup (zero or more items) goes here -->

<main>
  <nav>
    <div class="nav-wrapper">
        <i on:click={navbarResponsive} class=" right material-icons">menu</i>
      <span class="title left brand-logo">
        <Link to="/">Iglesia Emanuel</Link>
      </span>
      <ul id="nav-mobile" class="right links-responsive">
        {#each routes as {name,route}}
                <li><Link to={route}>{name}</Link></li>
        {/each}

      </ul>
    </div>
  </nav>

  <div class={rNav == false ? "side" : "sidebar"}>
    <ul class="ul-links-res">
      {#each routes as {name,route}}
        <li><Link to={route}><span class="link-nav-res">{name}</span></Link></li>
      {/each}
    </ul>
  </div>
</main>

<style>
  /* your styles go here */
  nav {
    background-color: cadetblue;
    overflow: hidden;
    position: fixed;
    width: 100%;
    top: 0;
    padding-left: 1.9px;
    padding-right: 2px;
    z-index: 100;
  }
  .link-nav-res{
    color: white;
    font-size: 20px;
  }
  .ul-links-res{
    display: flex;
    flex-wrap: wrap;
  }
  .ul-links-res li{
    margin-left: 10px;
  }
  .sidebar {
    background-color: rgb(115, 185, 187);
    height: 100px;
    top: 60px;
    width: 100%;
    right: 0;
    position: fixed;
    transition: all 0.6s;
    z-index: 1;
  }
  .side {
    background-color: rgb(115, 185, 187);
    height: 300px;
    width: 100%;
    position: fixed;
    transition: all 1s;
    top: -300px;
  }
  .material-icons {
    font-size: 40px;
    display: none;
  }
  @media only screen and (max-width: 601px) {
    nav {
      height: 10vh;
    }
    .sidebar {
    height: 90px;
    top: 50px;
    width: 100%;
    right: 0;
    position: fixed;
    transition: all 0.6s;
    z-index: 1;
  }
    
  }
  @media only screen and (max-width: 581px) {
    .material-icons {
      font-size: 40px;
      display: block;
    }
    nav {
      height: 9.6vh;
    }
    .links-responsive {
      display: none;
    }
  }
  @media only screen and (max-width: 503px) {
    .title {
      font-size: 29px;
    }
    nav {
      height: 11vh;
    }
  }
  @media only screen and (max-width: 430px) {
    .title {
      font-size: 26px;
      font-weight: bold;
    }
    nav {
      height: 8.6vh;
    }
    .sidebar {
    top: 46px;
    width: 100%;
    right: 0;
    position: fixed;
    transition: all 0.6s;
    z-index: 1;
  }
  }
  @media only screen and (max-width: 380px) {
    .title {
      font-size: 24px;
      font-weight: bold;
    }
    nav {
      height: 8.6vh;
    }
  }
  @media only screen and (max-width: 346px) {
    .title {
      font-size: 23px;
      font-weight: bold;
    }
    nav {
      height: 11vh;
    }
    .sidebar {
    top: 50px;
    width: 100%;
    right: 0;
    position: fixed;
    transition: all 0.6s;
    z-index: 1;
  }
  }
  @media only screen and (max-width: 281px) {
    .title {
      font-size: 19px;
      font-weight: bolder;
    }
    nav {
      height: 10.6vh;
    }
    .sidebar {
    top: 55px;
    width: 100%;
    right: 0;
    position: fixed;
    transition: all 0.6s;
    z-index: 1;
  }
  }
  @media only screen and (max-width: 277px) {
    .title {
      font-size: 19px;
      font-weight: bolder;
    }
    nav {
      height: 11vh;
    }
  }
  @media only screen and (max-width: 241px) {
    .title {
      font-size: 17px;
      font-weight: bolder;
    }
    nav {
      height: 11vh;
    }
  }
  @media only screen and (max-width: 206px) {
    .title {
      font-size: 16px;
      font-weight: bolder;
    }
    nav {
      height: 11vh;
    }
  }
</style>
