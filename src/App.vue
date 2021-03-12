<template>
  <div id="app">
    <b-row>
      <b-col cols="12" md="3" lg="2" offset-md="1">
        <sidebar/>
      </b-col>
      <b-col md="7" lg="8" class="text-left">
        <profile class="bg-light p-4 mb-5"/>
        <experience class="bg-light p-4 mb-5"/>
        <projects class="bg-light p-4 mb-5"/>
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
