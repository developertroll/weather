<template lang="">
  <header class="header">
    <h2>Weather Application</h2>
    <p>{{ userName }}님 반갑습니다!</p>
  </header>
</template>
<script>
export default {
  name: "HeaderDisplay",
  data() {
    return {
      userName: "김코딩",
    };
  },
};
</script>
<style scoped>
.header {
  background: #355c7d; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #c06c84,
    #6c5b7b,
    #355c7d
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #c06c84,
    #6c5b7b,
    #355c7d
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}
.header h2 {
  color: #fff;
}
.header p {
  font-size: 12px;
  color: #fff;
}
</style>
