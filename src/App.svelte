<script>
  	import { onMount } from 'svelte';
	import  NavBar from './NavBar.svelte';
	import GalleryContainer from './GalleryContainer.svelte';

	let arts = [];
	let count = 1;

	onMount( () => {
		fetch(`https://api.harvardartmuseums.org/object?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d`)
		.then(res => res.json())
		.then(data => arts = data.records)
		.then(error => console.log(error))
	})

	const nextGallery = () => {
		fetch(`"https://api.harvardartmuseums.org/object?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d&page={${count}}"`)
		.then(res => res.json())
		.then(data => arts = data.records)
		.then(error => console.log(error))
	}

</script>

<main>
  <NavBar />
  <GalleryContainer arts={arts} />


</main>

<style>

	
</style>