<script>
  import { onMount } from "svelte";
  import CircularIndicator from "../components/Circular_Indicator.svelte";
  // your script goes here
  export let dia = "";

  let loading = true;
  let listSongs = [];
  let findSONG = `https://songs-emanuel.herokuapp.com/songs`;

  onMount(async () => {
    const res = await fetch(findSONG);
    const box = await res.json();
    listSongs = box;

    loading = false;
  });
</script>

<!-- markup (zero or more items) goes here -->
<main>
  {#if loading == true}
    <CircularIndicator />
  {:else}
    <h2 class="center">Alabanzas</h2>
    {#each listSongs as song}
      {#if song.dia == dia}
        {#if song.type == "Alabanza"}
          <li class="collection-item">
            <div>
              <span class="title">{song.name}</span>
              <p>{song.autor}</p>
            </div>
            <div class="container-icon">
              <a href={song.link} target="_blank" class="secondary-content"
                ><i class="fab fa-youtube" /></a
              >
            </div>
          </li>
          <hr />
        {/if}
      {:else}
        <div />
      {/if}
    {/each}
    <h2 class="center">Adoracion</h2>
    {#each listSongs as song}
      {#if song.dia == dia}
        {#if song.type == "Adoración"}
          <li class="collection-item">
            <div>
              <span class="title">{song.name}</span>
              <p>{song.autor}</p>
            </div>
            <div class="container-icon">
              <a href={song.link} target="_blank" class="secondary-content"
                ><i class="fab fa-youtube" /></a
              >
            </div>
          </li>
          <hr />
        {/if}
      {:else}
        <div />
      {/if}
    {/each}
  {/if}
</main>

<style>
  /* your styles go here */

  .collection-item {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .container-icon {
    display: flex;
    align-items: center;
  }
  .fa-youtube {
    font-size: 30px;
    color: red;
  }
  .collection-item {
    padding-left: 3vh;
    padding-right: 3vh;
  }
  .title {
    font-size: 26px;
    color: #3e2723;
  }
  p {
    color: #757575;
  }
  @media only screen and (max-width: 286px) {
    h2 {
      font-size: 45px;
    }
    .title {
      font-size: 20px;
    }
  }
  @media only screen and (max-width: 234px) {
    h2 {
      font-size: 35px;
    }
    .title {
      font-size: 17px;
    }
  }
  @media only screen and (max-width: 179px) {
    h2 {
      font-size: 30px;
    }
    .title {
      font-size: 15px;
    }
  }
</style>
