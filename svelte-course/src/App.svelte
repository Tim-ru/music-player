<script>
	let name = 'svelte';
	let number = 42
	let src = 'https://www.nastol.com.ua/large/202004/396189.jpg'
	let altText = 'Mountains image'

	let htmlString = '<b>This is strong text </b> with <i>italic text</i>'
</script>

<main>
	<h1>Hello {name}!</h1>
	<h2>{name.toUpperCase()}</h2>
	<h2>{(Math.random() * number).toFixed(3)}</h2>
	<img {src} alt={altText} />

	<p>{@html htmlString}</p>
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
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	:global(img) {
		width: 180px;
		height: auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>