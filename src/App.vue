<template>
  <div id="app">
    Hello Vue.JS
    <hr />
    <span>Привет Vue.js</span>
    <hr />

    <first-component />
  </div>
</template>

<script>
import FirstComponent from "./components/FirstComponent.vue";

export default {
  components: { FirstComponent },
};
</script>

<style lang="scss" scoped>
div {
  font-size: 2rem;
  color: blue;
  span {
    color: green;
  }
}
</style>
