<script>
  import { onMount } from "svelte";
  import { Link } from "svelte-routing";
  import CircularIndicator from "../components/Circular_Indicator.svelte";
  let listCultos = [];
  let loading = true;
  let cultos=null;
  let APIURL = "https://songs-emanuel.herokuapp.com/cultos";
  onMount(async () => {
    const res = await fetch(APIURL);
    cultos = await res.json();
    listCultos = cultos;
    loading = false;
  });
</script>

<main>
  {#if loading == true}
    <CircularIndicator />
  {:else}
    <div>
      <div class="row">
        {#each listCultos as { _id, dia, description }}
          <div class="col s12 m6 l3">
            <div>
              <Link class="link-routes" to="/culto/{_id}/{dia}">
                <div class="card-panel teal lighten-3 center">
                  <span>
                    {dia}
                    <hr />
                    {description}
                  </span>
                </div>
              </Link>
            </div>
          </div>
        {/each}
      </div>
    </div>
  {/if}
</main>

<style>
  span {
    font-size: 30px;
    color: white;
  }
  hr {
    background-color: #b2dfdb;
    text-decoration: none;
    height: 1px;
    border: none;
  }
</style>
