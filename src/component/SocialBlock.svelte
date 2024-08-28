<script lang='ts'>
  export let url: string;
  export let imgUrl: string;
  export let label: string;
  export let imgAlt: string;
</script>

<a href={url}>
  <div class='social-block'>
    <img class='social-logo' src={imgUrl} alt={imgAlt}/>
    <span class='social-label'>{label}</span>
  </div>
</a>

<style>
  .social-block {
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .social-logo {
    height: 1.5rem;
  }

  .social-label {
    font-size: 1.5rem;
  }
</style>