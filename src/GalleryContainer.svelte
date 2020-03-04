<script>
  export let arts;
  
</script>

<section class='gallery'>
   {#each arts as art}
        <section class='paintings'>
            <img src={art.baseimageurl} alt='paintings'/>
        </section>
   {/each}
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
</style>