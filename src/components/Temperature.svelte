<script lang="ts">
  export let temperature: number | undefined = undefined;
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
  <span class="temperature-text">Temperature: {temperature || "N/A"}</span>
</div>

<style>
  .container {
    width: fit-content;
    border: 1px solid black;
    border-radius: 4px;
    padding: 12px 20px;
  }

  .temperature-text {
    font-weight: bold;
  }
</style>
