<script>
	import RandomCat from './components/RandomCat.svelte';
	import RandomFact from './components/RandomFact.svelte';
	import Sidebar from './components/Sidebar.svelte';
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: auto;
		width: 75vw;
		padding-top: 64px;
	}

	@media (max-width: 768px) {
		main {
			padding: 0;
			width: 95vw;
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