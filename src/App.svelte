<script lang="ts">
  import Temperature from './components/Temperature.svelte';
  import WordSplitter from './components/WordSplitter.svelte';
  import Header from './components/Header.svelte';
</script>

<Header />
<main>
  <Temperature />
  <p>
    <WordSplitter />
  </p>
</main>

<style>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    padding: 1em;
    margin: 0 auto;
  }
</style>
