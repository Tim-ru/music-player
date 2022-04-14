<script>
    export let name = "Undefined name";
    export let age = "Undefined age";
    export let job = "Undefined job";
</script>

<div>
    <p>Name: <b>{name}</b></p>
    <p>Job: <b>{job}</b></p>

    {#if age < 18}
        <p>This person can`t work</p>
        {:else}
        <p>This person can do anything</p>
    {/if}
</div>

<style>
    div {
        border: 1px solid black;
        padding: 1rem;
        margin-bottom: 1rem;
    }
</style>
