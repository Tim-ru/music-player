<script>
	let name = "Svelte";
	let counter = 0;
	$: counterClass = counter % 2 === 0 ? "red" : "blue";

	$: upperName = name.toUpperCase();
	$: lowerName = name.toLowerCase();

	$: {
		console.log("Name", name);
		console.log("Counter", counter);
	}

	$: if (counter === 10) {
		name = "Counter is equal 10";
	} else {
		name = 'Svelte';
	}

	function changeName() {
		name = "New name";
	}
</script>

<main>
	<h1>{name}</h1>
	<h2>{upperName}</h2>
	<h2>{lowerName}</h2>

	<button on:click={changeName}>Submit form</button>
	<h1 class={counterClass}>{counter}</h1>
	<button on:click={() => counter++}>Add 1 to counter</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		font-size: 4em;
		font-weight: 100;
	}

	.playground {
		width: 400px;
		height: 200px;
		padding: 1rem;
		margin-bottom: 1rem;
		border: 1px solid black;
	}
	.blue {
		color: #3f3fdf;
	}
	.red {
		color: #ff3e00;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
