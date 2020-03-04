<script>
  export let arts;
  
</script>

<section class='gallery'>
   <p>↠</p>
   {#each arts as art}
        <section class='paintings'>
            <img src={art.images[0].baseimageurl} alt='paintings'/>
            <p class='culture'>Culture: {art.culture}</p>
        </section>
   {/each}
   <p>↞</p>
</section>

<style>
	.gallery {
        background-color: #FEF7DE;
        height: 100vh;
        padding: 20px;
        display: flex;
        /* justify-content: center; */
        /* flex-wrap: wrap; */
        align-items: center;
        overflow-x: scroll;
    }

    .paintings {
        margin: 10px;
        padding: 10px;
        background-color: white;
        height: 30em;
    }

    img {
        height: 30em;
    }

    .culture {
        font-size: 20px;
    }

    p {
        margin: 5px;
        font-size: 5em;
    }
</style>