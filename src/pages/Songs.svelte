<script>
    // your script goes here
    import { onMount } from "svelte";
    import { Link } from "svelte-routing";
    import CircularIndicator from "../components/Circular_Indicator.svelte";
    let listBoxes = [];
    let loading = true;
    let APIURL = "https://songs-emanuel.herokuapp.com/boxes";
    onMount(async () => {
      const res = await fetch(APIURL);
      const boxes = await res.json();
      listBoxes = boxes;
      loading = false;
    });
  </script>
  
  <!-- markup (zero or more items) goes here -->
  
  <main>
    {#if loading == true}
      <CircularIndicator />
    {:else}
      <div>
        <div class="row">
          {#each listBoxes as { _id, dia }}
            <div class="col s12 m6 l3">
              <div class="gridlist">
                <Link class="link-routes" to="/detail/{_id}/{dia}">
                  <div class="card-panel teal lighten-3 center">
                    <span>
                      {dia}
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
  </style>
  