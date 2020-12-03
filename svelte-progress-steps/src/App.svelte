<script>
	let currentActive = 1;
	let enableActive;
	let circles = 4;
	let disabled;

	const previousHandler = () => {
		currentActive--;
		if (currentActive < 1) {
			currentActive = 1;
		}
		enbaleButtonHelper();
		desactivateHelper();
	};

	const nextHandler = () => {
		currentActive++;
		if (currentActive > circles) {
			currentActive = circles;
		}
		enableActiveHelper();
		enbaleButtonHelper();
	};

	const enableActiveHelper = () => {
		enableActive = !enableActive;
	};

	const desactivateHelper = () => {
		enableActive = false;
	};

	const enbaleButtonHelper = () => {
		if (currentActive === 1) {
			disabled = true;
		} else if (currentActive === circles) {
			disabled = true;
		} else {
			disabled = false;
		}
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
		{disabled}>Prev</button>
	<button on:click={nextHandler} class="btn" id="next">Next</button>
</div>
