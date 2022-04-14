<script>
	let name = "Svelte";
	let agree = true;
	let text = "";
	let select = "2";
	let sex = "male";
</script>

<main>
	<h1>{name}</h1>
	<input type="text" bind:value={name} />
	<hr />
	<input type="checkbox" bind:checked={agree} />
	{agree}
	<hr />
	<textarea bind:value={text} />
	<div style="white-space: pre-wrap;">{text}</div>
	<hr />
	<select bind:value={select}>
		<option value="0">option 0</option>
		<option value="1">option 1</option>
		<option value="2">option 2</option>
	</select>
	<hr />
	<input type="radio" value="female" bind:group={sex} />Female
	<input type="radio" value="male" bind:group={sex} />Male
	<br />
	Sex: {sex}
</main>

<style>
</style>
