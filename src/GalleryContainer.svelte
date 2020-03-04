<script>
  export let arts;
  
</script>

<section class='gallery'>
   {#each arts as art}
        <section>
            <img src={art.baseimageurl} alt='paintings'/>
        </section>
   {/each}
</section>

<style>
	.gallery {
        background-color: #FEF7DE;
        height: 100vh;
        padding: 20px;
    }
</style>