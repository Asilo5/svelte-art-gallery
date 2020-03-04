<script>
  import NextPage from './NextPage.svelte';
  export let pageNumber;
  export let nextGallery;
  
</script>

<nav> 
  <h1>La Lumbrera</h1>
  <div>
     <NextPage nextGallery={nextGallery} pageNumber={pageNumber}/> 
     <p>Favourites</p>
  </div>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    box-shadow: 0 5px 5px -3px gray;
    position: relative;
    z-index: 1;
  }

  h1 {
    font-family: 'Trade Winds', cursive;
    font-size: 20px;
  }

  p {
    font-weight: 100;
  }

  div {
    display: flex;
  }
	
</style>