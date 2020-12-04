<script>
	let currentActive = 1;
	let previousEnableActive;
	let nextEnableActive;
	let circles = [1, 2, 3, 4];
	let previousDisabled;
	let nextDisabled;

	const previousHandler = () => {
		currentActive--;
		if (currentActive < 1) {
			currentActive = 1;
		}
		buttonHelper();
	};

	const nextHandler = () => {
		currentActive++;
		if (currentActive > circles.length) {
			currentActive = circles.length;
		}
		buttonHelper();
	};

	const previousEnableActiveHelper = () => {
		previousEnableActive = !previousEnableActive;
	};

	const nextEnableActiveHelper = () => {
		nextEnableActive = !nextEnableActive;
	};

	const buttonHelper = () => {
		if (currentActive === 1) {
			previousDisabled = true;
		} else if (currentActive === circles.length) {
			nextDisabled = true;
		} else {
			previousDisabled = false;
			nextDisabled = false;
		}
	};
</script>

<style>
</style>

<div class="container">
	<div class="progress-container">
		<div class="progress" id="progress" />
		<div class="circle active">1</div>
		<div class={previousEnableActive ? ' circle active' : 'circle'}>2</div>
		<div class="circle">3</div>
		<div class="circle">4</div>
	</div>

	<button
		on:click={previousHandler}
		class="btn"
		id="prev"
		disabled={previousDisabled}>Prev</button>

	<button
		on:click={nextHandler}
		class="btn"
		id="next"
		disabled={nextDisabled}>Next</button>
</div>
