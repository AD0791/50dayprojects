<script>
	let currentActive = 1;
	let enableActive;
	const previousHandler = () => {};

	const nextHandler = () => {
		const circles = 4;
		currentActive++;
		if (currentActive > circles) {
			currentActive = circles;
		}
		enableActiveHandler();
	};

	const enableActiveHandler = () => {
		enableActive = !enableActive;
	};
</script>

<style>
</style>

<div class="container">
	<div class="progress-container">
		<div class="progress" id="progress" />
		<div class="circle active">1</div>
		<div class={enableActive ? ' circle active' : 'circle'}>2</div>
		<div class="circle">3</div>
		<div class="circle">4</div>
	</div>

	<button
		on:click={previousHandler}
		class="btn"
		id="prev"
		disabled>Prev</button>
	<button on:click={nextHandler} class="btn" id="next">Next</button>
</div>
