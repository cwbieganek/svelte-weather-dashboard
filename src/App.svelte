<script lang="ts">
  import Temperature from './components/Temperature.svelte'
  import WordSplitter from './components/WordSplitter.svelte';
</script>

<main>
  <Temperature />
  <p>
    <WordSplitter />
  </p>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    padding: 1em;
    margin: 0 auto;
  }
</style>
