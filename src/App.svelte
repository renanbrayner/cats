<script>
	import RandomCat from './components/RandomCat.svelte';
	import RandomFact from './components/RandomFact.svelte';
	import Sidebar from './components/Sidebar.svelte';
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: auto;
		width: 75vw;
		padding-top: 64px;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<Sidebar />
	<div class='content'>	
		<RandomCat />
		<RandomFact />
	</div>
</main>