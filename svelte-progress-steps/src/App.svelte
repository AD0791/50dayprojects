<script>
	let currentActive = 1;
	let active1 = true;
	let active2;
	let active3;
	let active4;
	let previousDisabled;
	let nextDisabled;
	let circles = [1, 2, 3, 4];

	const previousHandler = () => {
		currentActive--;
		if (currentActive < 1) {
			currentActive = 1;
		}
		buttonHelper();
		//previouscircleHelper();
	};

	const nextHandler = () => {
		currentActive++;
		if (currentActive > circles.length) {
			currentActive = circles.length;
		}
		buttonHelper();
		//nextcircleHelper();
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
	const nextcircleHelper = () => {
		circles.forEach((c) => {
			if (c === 2) {
				active2 = true;
			}
			if (c === 3) {
				active3 = true;
			}
			if (c === 4) {
				active4 = true;
			}
		});
	};
	const previouscircleHelper = () => {
		circles.forEach((c) => {
			if (c === 2) {
				active2 = false;
			}
			if (c === 3) {
				active3 = false;
			}
			if (c === 4) {
				active4 = false;
			}
		});
	};
</script>

<style>
</style>

<div class="container">
	<div class="progress-container">
		<div class="progress" id="progress" />
		<div class={active1 ? ' circle active' : 'circle'}>1</div>
		<div class={active2 ? ' circle active' : 'circle'}>2</div>
		<div class={active3 ? ' circle active' : 'circle'}>3</div>
		<div class={active4 ? ' circle active' : 'circle'}>4</div>
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
