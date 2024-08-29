<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin=''>
<link href="https://fonts.googleapis.com/css2?family=Luckiest+Guy&family=Quicksand:wght@300..700&display=swap" rel="stylesheet">

<script lang="ts">
  import Header from "./component/Header.svelte";
  import ProjectWindow from "./component/ProjectWindow.svelte";
  import projectJson from './assets/projects.json'

  const projects = projectJson.projects;
</script>

<main>
  <Header />
  <ProjectWindow {projects} />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100dvh;
    padding: 8px;
    box-sizing: border-box;
    background: url('bg.jpg') center / cover fixed;
  }
  
  @media (min-width: 640px) {
    main {
      min-width: 624px;
    }
  }
</style>
