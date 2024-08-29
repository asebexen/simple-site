<script>
  import SocialBlock from "./SocialBlock.svelte";
  import twitterLogo from '../assets/twitter-logo.svg';
  import githubLogo from '../assets/github-logo.svg'
</script>
<header>
  <h1>
    Arden Sebexen
  </h1>
  <div class='socials-bar'>
    <SocialBlock url='https://x.com/asebexen' imgUrl={twitterLogo} label='asebexen' imgAlt='X logo' />
    <SocialBlock url='https://github.com/asebexen' imgUrl={githubLogo} label='asebexen' imgAlt='Github logo' />
  </div>
</header>

<style>
  header {
    display: flex;
    flex-direction: column;
  }

  .socials-bar {
    display: flex;
    gap: 2rem;
    justify-content: center;
    background: #fad8beb3;
    border-radius: 0.25rem;
    align-items: center;
    padding: 0.5rem 0px;
    margin-bottom: 1rem;
  }

  h1 {
    font-family: 'Luckiest Guy', cursive;
    font-weight: 100;
    font-size: 3rem;
    text-align: center;
    margin-block: 0px;
    padding: 1rem 0rem 0.25rem;
  }
</style>