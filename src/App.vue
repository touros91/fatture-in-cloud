<template>
  <div id="app">
    <Months />
  </div>
</template>

<script>
import Months from "./components/Months.vue";

export default {
  name: "App",
  components: {
    Months,
  },
};
</script>

<style>
#app {
  font-family: "Inter", sans-serif;
  font-family: "Lato", sans-serif;
  margin-top: 60px;
}
</style>
