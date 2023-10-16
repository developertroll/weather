<template lang="">
  <div>
    <ul class="CitySelector">
      <li
        @click="selectCity(city)"
        :class="{ isSelected: city.selected }"
        v-for="city in cities"
        :key="city.code"
      >
        {{ city.name }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "CitySelector",
  data() {
    return {
      cities: [
        { code: "Seoul", name: "서울", selected: false },
        { code: "Tokyo", name: "도쿄", selected: false },
        { code: "Dubai", name: "두바이", selected: false },
        { code: "Beijing", name: "베이징", selected: false },
        { code: "Sydney", name: "시드니", selected: false },
        { code: "Paris", name: "파리", selected: false },
        { code: "London", name: "런던", selected: false },
        { code: "Moscow", name: "모스크바", selected: false },
        { code: "Bangkok", name: "방콕", selected: false },
      ],
    };
  },
  methods: {
    selectCity(city) {
      city.selected = !city.selected;
      this.$emit("selectCity", city);
    },
  },
};
</script>
<style scoped>
.CitySelector {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
}
.CitySelector li {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 0.05rem solid #efefef;
  padding: 0.3rem;
  cursor: pointer;
}
.isSelected {
  background: #fd1d1d;
  color: #fff;
}
</style>
