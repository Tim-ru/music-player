<script>
	import Person from "./Person.svelte";
	const people = [
		{id: 1, name: 'John', age: '21', job: 'Frontend'},
		{id: 2, name: 'Helena', age: '17', job: 'Student'},
	]
</script>

<h1>Application</h1>

<Person {...people[0]} />
<Person {...people[1]} />
