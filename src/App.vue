<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <BlogPage />
  </div>
</template>

<script>
import BlogPage from "./components/BlogPage.vue";

export default {
  name: "App",
  components: {
    BlogPage,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Rubik&display=swap");
#app {
  font-family: "Rubik", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 color: #111111;
  font-size: 18px;
}
* {
  padding: 0px;
  margin: 0px;
}
</style>
