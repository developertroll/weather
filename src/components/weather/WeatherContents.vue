<template lang="">
  <h2>Weather Contents</h2>
  <ContentHeader />
  <CitySelector @selectCity="selectCity" />
  <WeatherList :weatherList="weatherList" />
</template>
<script>
import ContentHeader from "./ContentHeader.vue";
import CitySelector from "./CitySelector.vue";
import WeatherList from "./WeatherList.vue";
import WeatherMixin from "../mixins/WeatherMixin";
export default {
  name: "WeatherContents",
  components: {
    ContentHeader,
    CitySelector,
    WeatherList,
  },
  mixins: [WeatherMixin],
  data() {
    return {
      weatherList: [],
    };
  },
  methods: {
    async selectCity(city) {
      if (city.selected) {
        const weather = await this.getWeatherInfo(city);
        this.weatherList.push(weather);
      } else {
        const index = this.weatherList.findIndex(
          (weather) => weather.code === city.code
        );
        this.weatherList.splice(index, 1);
      }
    },
  },
};
</script>
<style lang=""></style>
