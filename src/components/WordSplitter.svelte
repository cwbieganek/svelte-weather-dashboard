<script lang="ts">
  let text = "";
  let words: string[];
  $: words = text.split(" ");
</script>

<div class="container">
  <label for="word-splitter">Word Splitter: </label>
  <input type="text" bind:value={text} />
  {#each words as word, i}
    {#if word != ""}
      <div><span>Word {i + 1}: {word}</span></div>
    {/if}
  {/each}
</div>

<style>

</style>
