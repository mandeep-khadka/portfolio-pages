<script>
    import PageHeader from "$lib/components/PageHeader.svelte";
    import Project from "$lib/components/Project.svelte";
    import projects from "$lib/data/projects";
</script>

<PageHeader title="Projects" />

<div class="container">
    {#each projects as project}
        <Project {project}/>
    {/each}
</div>