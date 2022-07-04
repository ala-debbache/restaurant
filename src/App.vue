<template>
  <v-app>
    <HomePage />
  </v-app>
</template>

<script>
import HomePage from "./views/home/Index";

export default {
  name: "App",

  components: {
    HomePage,
  },
};
</script>
<style>
#app {
  width: 100%;
}
</style>