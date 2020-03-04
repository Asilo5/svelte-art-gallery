<script>
  export let arts;
  
</script>

<section class='gallery'>
   <p>↠</p>
   {#each arts as art}
        <section class='paintings'>
            <img src={art.images[0].baseimageurl} alt='paintings'/>
            <article>
                <p>{art.title}</p>
                <p>Culture: {art.culture}</p>
                <p >Dated: {art.dated} </p>
            </article>
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
        overflow-x: scroll;
    }

    .paintings {
        margin: 15px;
        padding: 15px;
        border-radius: 5px;
        background: linear-gradient( to left, #d6a73e 22%,#d2a559 25%, #d4bc83 40%, #e3ba62 31%,#d8af32 45%,#d09532 80%) left bottom transparent no-repeat;
        height: 30em;
    }

    article{
      text-align: center;
      margin-top: 20px;
      padding: 10px;
      border: 1px solid black;
      background-color: white;
    }

    article > p {
        margin: 10px;
        font-size: 20px;
    }

    img {
        height: 30em;
        border: 2px solid black;
    }

    p {
        margin: 5px;
        font-size: 5em;
    }
</style>