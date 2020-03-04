<script>
  	import { onMount } from 'svelte';
	import  NavBar from './NavBar.svelte';
	import GalleryContainer from './GalleryContainer.svelte';

	let arts = [];
	let pageNumber = 2;

	onMount( () => {
		fetch(`https://api.harvardartmuseums.org/object?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d`)
		.then(res => res.json())
		.then(data => arts = data.records)
		.then(error => console.log(error))
	})

	const nextGallery = () => {
		fetch(`https://api.harvardartmuseums.org/object?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d&page=${pageNumber}`)
		.then(res => res.json())
		.then(data => arts = data.records)
		.then(error => console.log(error))
	}

</script>

<main>
  <NavBar nextGallery={nextGallery} pageNumber={pageNumber} />
  {#if arts.length === 0}
    <img src='https://i.pinimg.com/originals/a4/f2/cb/a4f2cb80ff2ae2772e80bf30e9d78d4c.gif' alt='loading giph' /> 
  {:else}
  <GalleryContainer arts={arts} />
  {/if}


</main>

<style>
  img {
	display: block;
	margin: 15em auto;
  }
	
</style>