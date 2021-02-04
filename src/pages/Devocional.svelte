<script>
    import { onMount } from "svelte";
    import { Link } from "svelte-routing";
    import CircularIndicator from "../components/Circular_Indicator.svelte";
    let listDevocionales = [];
    let loading = true;
    let APIURL = "https://songs-emanuel.herokuapp.com/devocionales";
    onMount(async () => {
        const res = await fetch(APIURL);
        const devocionales = await res.json();
        listDevocionales = devocionales;
        loading = false;
    });
</script>

<style>
    .title-dia {
        font-size: 49px;
        color: white;
        font-weight: bold;
    }

    .title-fecha {
        font-size: 30px;
        color: rgb(124, 132, 138);
    }
    .link-text {
        color: azure;
        font-weight: bold;
        font-size: 16px;
    }
    .link-text:hover{
        color: #b2ffef;
    }
    .fa-angle-double-right{
        margin-left: 3px;
    }


</style>

<main>
    {#if loading == true}
        <CircularIndicator />
        {:else}
        <div class="row">
            {#each listDevocionales as {_id,dia,fecha,frameurl}}
                <div class="col s12 m6 l4">
                    <div class="center card">
                        <div class="card-content teal lighten-3 center white-text">
                            <span class="title-dia card-title">{dia}</span>
                            <span class="title-fecha">{fecha}</span>
                        </div>
                        <div class="card-action teal lighten-3 center">
                            <Link to="/devocional/{_id}">
                                <span class="link-text">ir al devocional<i class="fas fa-angle-double-right"></i></span>
                            </Link>
                        </div>
                    </div>
                </div>
            {/each}
        </div>

    {/if}
</main>