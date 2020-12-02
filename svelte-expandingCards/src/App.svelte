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
	let forestActiveHandler = () => (forestActive = !forestActive);
	let beachActiveHandler = () => (beachActive = !beachActive);
	let cityActiveHandler = () => (cityActive = !cityActive);
	let mountainActiveHandler = () => (mountainActive = !mountainActive);
	let wordActiveHandler = () => (wordActive = !wordActive);
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
