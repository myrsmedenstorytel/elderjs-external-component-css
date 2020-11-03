<script>
  import { Button } from 'test-external-svelte-library';

  export let data, helpers;
</script>

<style>
  a {
    margin-bottom: 1rem;
    display: inline-block;
  }
</style>

<svelte:head>
  <title>{data.title}</title>
</svelte:head>

<a href="/">&LeftArrow; Home</a>

<h1>{data.title}</h1>
<Button>Even better if you click here</Button>
<ul>
  {#each data.steps as step}
    <li>{step}</li>
  {/each}
</ul>

{@html data.content}
