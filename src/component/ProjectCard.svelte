<script lang='ts'>
    import type { Project } from "../types";

  export let project: Project;
</script>

<div class='project-card'>
  <h2 class='project-name'>{project.name}</h2>
  <div class='project-description'>
    {project.description}
  </div>
  <div class='project-links'>
    <div>
      {#if project.repoUrl}
        <a href={project.repoUrl}>Repository</a>
      {/if}
    </div>
    <div>
      {#if project.deployUrl}
        <a href={project.deployUrl}>Deploy</a>
      {/if}
    </div>
  </div>
</div>

<style>
  .project-name {
    margin-block: 0px;
  }

  .project-description {
    flex: 1 1 0px;
  }
  
    .project-links {
      display: flex;
      justify-content: space-between;
    }

  @media (min-width: 640px) {
    .project-name {
      padding: 0rem 2rem;
    }
  
    .project-description {
      padding: 0rem 1rem;
    }

    .project-links {
      padding: 0.25rem 1rem;
    }
  }

  .project-card {
    margin: 0.25rem;
    background-color: #f4dbccd8;
    padding: 0.25rem;
    border-radius: 0.25rem;
    box-shadow: 0px 1px 4px #7a081f70;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 1rem;
  }
</style>