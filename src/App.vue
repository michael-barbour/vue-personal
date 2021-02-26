<template>
  <div id="app" class="container-fluid">
    <b-row>
      <b-col cols="12" md="3" offset-md="1" class="bg-light">
        <sidebar/>
      </b-col>
      <b-col md="7" class="text-left bg-light">
        <profile/>
        <experience/>
        <projects/>
      </b-col>
    </b-row>
  </div>
</template>

<script>

import Sidebar from "@/components/Sidebar";
import Profile from "@/components/Profile/Profile";
import Experience from "@/components/Experience/Experience";
import Projects from "@/components/Project/Project";

export default {
  name: 'App',
  components: {
    Projects,
    Experience,
    Profile,
    Sidebar
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
  background: #3d3d3d;
  min-height: 100vh;
}
</style>
