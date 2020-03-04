<script>
    export let pageNumber;
    export let nextGallery;
</script>


<section>
    <button on:click={() => {
        console.log(pageNumber)
        pageNumber--;
        nextGallery();
        }}> Previous Art </button>


    <button on:click={() => {
        console.log(pageNumber)
        pageNumber++;
        nextGallery();
        }} > Next Art</button>
</section>

<style>
  button {
      font-size: 16px;
      font-family: 'Nunito', sans-serif;
      color: black;
      border: none;
      margin-right: 10px;
      margin-top: -5px;
      cursor: pointer;
  }

  button:hover {
      text-decoration: underline;
  }
	
</style>