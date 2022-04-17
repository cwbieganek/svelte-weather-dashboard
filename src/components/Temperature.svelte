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

<div class="w-fit rounded-md border border-solid border-black px-4 py-2">
  <span class="font-bold">Temperature: {temperature || "N/A"}</span>
</div>

<style>

</style>
