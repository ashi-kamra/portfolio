<script>
    import projects from "$lib/projects.json";
    import Project from "$lib/Project.svelte";

</script>

<svelte:head>
    <h1>my projects</h1>
</svelte:head>

{#each projects as p}
    <Project data={p} />
{/each}