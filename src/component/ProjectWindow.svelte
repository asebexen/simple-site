<script lang='ts'>
    import type { Project } from "../types";
    import ProjectCard from "./ProjectCard.svelte";

  const projectSort = (a: Project, b: Project): number => {
    if (a.rating > b.rating) return -1;
    else if (a.rating < b.rating) return 1;

    if (a.deployUrl && !b.deployUrl) return -1;
    else if (!a.deployUrl && b.deployUrl) return 1;

    if (a.repoUrl && !b.repoUrl) return -1;
    else if (!a.repoUrl && b.repoUrl) return 1;

    if (a.name > b.name) return 1;
    else if (a.name < b.name) return -1;

    return 0;
  }

  export let projects: Project[];
  $: sortedProjects = projects.sort(projectSort)
</script>

<div class='project-window'>
  {#each sortedProjects as project (project.name)}
    <ProjectCard {project} />
  {/each}
</div>

<style>
  .project-window {
    overflow-y: auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem;
  }

  @media (min-width: 640px) {
    .project-window {
      grid-template-columns: 1fr 1fr 1fr;
    }
  }
  
  @media (min-width: 960px) {
    .project-window {
      grid-template-columns: 1fr 1fr 1fr 1fr;
    }
  }
</style>