<script lang="ts">
  export let temperature: number;
  let temperatureColor: string;
  $: temperatureColor = getColorForTemperature(temperature);

  function getColorForTemperature(temperature: number): string {
    if (temperature <= 32.0) {
      return "#E0FFFF";
    }

    if (temperature <= 60) {
      return "#F0E68C";
    }

    if (temperature <= 80) {
      return "#FFA500";
    }

    return "#FF0000";
  }
</script>

<div class="container">
  <p class="temperature-text" style="--temperature-color: {temperatureColor}">Temperature: {temperature || ""}</p>
  <div>
    <label for="temperature">Enter a temperature: </label><input type="number" name="temperature" bind:value={temperature} />
  </div>
</div>

<style>
  .container {
    width: fit-content;
    border: 1px solid black;
    border-radius: 4px;
    padding: 12px 20px;
    background-color: black;
  }

  .temperature-text {
    color: var(--temperature-color);
    font-weight: bold;
  }

  label {
    color: white;
  }
</style>
