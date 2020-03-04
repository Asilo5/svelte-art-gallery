<script>
  	import { onMount } from 'svelte';
	import  NavBar from './NavBar.svelte';

	let arts = [];

	onMount(async () => {
		const res = await fetch(`https://api.harvardartmuseums.org/image?apikey=30de38c0-5cb4-11ea-9401-ed9c8b78a90d`);
		let allPaints = await res.json();
		arts = allPaints.records;
		console.log('arts', arts)   
	});
</script>

<main>
  <NavBar />


</main>

<style>
	
</style>