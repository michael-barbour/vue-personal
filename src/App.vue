<template>
  <b-container id="app">
    <profile class="bg-light p-4 mb-5" />
    <experience class="bg-light p-4 mb-5" />
    <projects class="bg-light p-4 mb-5" />
  </b-container>
</template>

<script>

import Profile from "@/components/Profile/Profile";
import Experience from "@/components/Experience/Experience";
import Projects from "@/components/Project/Project";

export default {
  name: 'App',
  components: {
    Projects,
    Experience,
    Profile,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1f2d39;
  padding-top: 60px;
  min-height: 100vh;
}

body {
  background-image: url("assets/chicago-skyline.jpg");
  background-attachment: fixed;
  background-size: cover;
  background-repeat: no-repeat;
}

</style>
