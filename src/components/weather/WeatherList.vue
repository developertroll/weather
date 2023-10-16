<template lang="">
  <div>
    <ul class="weather-list">
      <WeatherItem
        v-for="weather in weatherList"
        :key="weather.code"
        :weather="weather"
      />
    </ul>
  </div>
</template>
<script>
import WeatherItem from "./WeatherItem.vue";
export default {
  name: "weather-list",
  components: {
    WeatherItem,
  },
  props: {
    weatherList: Array,
  },
};
</script>
<style scoped>
.weather-list {
  display: grid;
  margin-top: 1rem;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 1rem;
}
</style>
