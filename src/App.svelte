<script>
  	import { onMount } from 'svelte';
	import  NavBar from './NavBar.svelte';
	import GalleryContainer from './GalleryContainer.svelte';

	let arts = [];

	// onMount(async () => {
		// const res = await fetch(`https://api.harvardartmuseums.org/image?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d`);
		// let allPaints = await res.json();
		// arts = allPaints.records;
		// arts.push(...allPaints.records);
		// console.log('arts', arts)   
	// });

	onMount( () => {
		fetch(`https://api.harvardartmuseums.org/image?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d`)
		.then(res => res.json())
		.then(data => arts = data.records)
		.then(error => console.log(error))
	})
</script>

<main>
  <NavBar />
  <GalleryContainer arts={arts} />


</main>

<style>

	
</style>