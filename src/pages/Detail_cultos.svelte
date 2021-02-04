<script>
    // your script goes here
    import {onMount} from "svelte";

    export let id = null;
    let culto = [];
    let videos = [];
    let loading = true;
    onMount(async () => {
        const resCulto = await fetch(
            `https://songs-emanuel.herokuapp.com/culto/${id}`
        );
        const resVideos = await fetch("https://songs-emanuel.herokuapp.com/videos");
        culto = await resCulto.json();
        videos = await resVideos.json();
        console.log(culto);
        console.log(videos);
        loading = false;
    });
</script>

<!-- markup (zero or more items) goes here -->
<main>
    {#if loading == false}
        <div class="center">
            <span class="col s12 center titleSize">{culto.dia}</span>
            <span class=" descriptionSize">{culto.description}</span>
            <span class=" descriptionSize">{culto.hora}</span>
        </div>
        <hr/>
        <div class="row">
            {#each videos as {dia, fecha, videourl}}
                {#if dia == culto.dia}
                    <div class="col s12 m6 l3">
                        <div class="center card">
                            <div class="card-content white-text">
                                <span class="title-dia card-title">{dia}</span>
                                <span class="title-fecha">{fecha}</span>
                            </div>
                            <div class="card-action">
                                <a target="_blank" class="link-style" href={videourl}>
                                    <i class="fab fa-facebook"/>
                                    <span class="link-text">ver el culto</span>
                                </a>
                            </div>
                        </div>
                    </div>
                {/if}
                <div></div>
            {/each}
        </div>
    {/if}
</main>

<style>
    /* your styles go here */
    .titleSize {
        font-size: 70px;
    }

    .link-style {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .link-text {
        color: rgb(45, 145, 192);
        font-size: 17px;
        font-weight: 500;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;

    }

    .descriptionSize {
        font-size: 50px;
        color: gray;
    }

    .center {
        display: flex;
        flex-direction: column;
    }

    hr {
        background: linear-gradient(-10deg, cadetblue, rgb(94, 165, 191) 150%);
        height: 4px;
        border-radius: 10px;
        border: none;
    }

    .title-dia {
        font-size: 40px;
        color: rgb(35, 115, 149);
    }

    .title-fecha {
        font-size: 25px;
        color: rgb(105, 164, 187);
    }

    .fab {
        font-size: 40px;
        padding-right: 3px;
        color: rgb(45, 145, 192);
    }
    @media only screen and (max-width: 393px){
        .descriptionSize{
            font-size: 40px;
        }
    }
    @media only screen and (max-width: 309px){
        .descriptionSize{
            font-size: 30px;
        }
        .titleSize{
            font-size: 60px;
        }
    }
    @media only screen and (max-width: 227px){
        .descriptionSize{
            font-size: 20px;
        }
        .titleSize{
            font-size: 50px;
        }
    }
</style>
