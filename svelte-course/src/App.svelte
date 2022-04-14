<script>
	let value = "Hello";
	$: error = isValid(value);
	function isValid(val) {
		return val.length > 5 && val.length < 10;
	}
</script>

<main>
	<h1>Application {value}</h1>
	<input type="text" bind:value class:red={error} class:green={!error} />
</main>

{#if value.length < 5}
	<p>text 1</p>
{:else if value.length > 10}
	<p>text 2</p>
{/if}

<style>
	input {
		outline: none;
	}
	.red {
		border: red 1px solid;
	}
	.green {
		border: green 1px solid;
	}
</style>
