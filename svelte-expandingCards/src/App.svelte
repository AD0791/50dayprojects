<script>
	import Beach from "./components/Beach.svelte";
	import City from "./components/City.svelte";
	import Forest from "./components/Forest.svelte";
	import Mountains from "./components/Mountains.svelte";
	import World from "./components/World.svelte";
	let wordActive;
	let forestActive;
	let beachActive;
	let cityActive;
	let mountainActive;
	const forestActiveHandler = () => (forestActive = !forestActive);
	const beachActiveHandler = () => (beachActive = !beachActive);
	const cityActiveHandler = () => (cityActive = !cityActive);
	const mountainActiveHandler = () => (mountainActive = !mountainActive);
	const wordActiveHandler = () => (wordActive = !wordActive);
</script>

<style>
</style>

<div class="container">
	<World {wordActive} on:click={wordActiveHandler} />
	<Forest {forestActive} on:click={forestActiveHandler} />
	<Beach {beachActive} on:click={beachActiveHandler} />
	<City {cityActive} on:click={cityActiveHandler} />
	<Mountains {mountainActive} on:click={mountainActiveHandler} />
</div>
