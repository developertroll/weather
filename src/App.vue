<template>
  <HeaderDisplay />
  <WeatherContents />
</template>

<script>
import HeaderDisplay from "./components/layouts/HeaderDisplay.vue";
import WeatherContents from "./components/weather/WeatherContents.vue";
export default {
  name: "App",
  components: {
    HeaderDisplay,
    WeatherContents,
  },
};
</script>

<style></style>
