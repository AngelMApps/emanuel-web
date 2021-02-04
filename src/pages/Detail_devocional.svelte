<script>
    import {onMount} from "svelte";
    import CircularIndicator from "../components/Circular_Indicator.svelte";

    export let id = null;
    let devocional = [];
    let loading = true;
    onMount(async () => {
        const resCulto = await fetch(
            `https://songs-emanuel.herokuapp.com/devocional/${id}`
        );
        devocional = await resCulto.json();
        loading = false;
    });
</script>

<style>
    main {
        background-color: #f9fffe;
        height: 90.5vh;
    }
</style>

<main>
    {#if loading == true}
        <CircularIndicator />
        {:else}
        <iframe title="{devocional.dia}" src={devocional.frameurl} width="100%" height="100%" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
    {/if}
</main>