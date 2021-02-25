<template>
  <div id="app" class="container-fluid">
    <b-row>
      <b-col cols="12" md="3" offset-md="1">
        <sidebar/>
      </b-col>
      <b-col md="7" class="text-left">
        <profile/>
        <work-history/>
        <education/>
        <projects/>
      </b-col>
    </b-row>
  </div>
</template>

<script>

import Sidebar from "@/components/Sidebar";
import Profile from "@/components/Profile/Profile";
import WorkHistory from "@/components/WorkHistory/WorkHistory";
import Education from "@/components/Education/Education";
import Projects from "@/components/Project/Project";

export default {
  name: 'App',
  components: {
    Projects,
    Education,
    WorkHistory,
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
  color: #2c3e50;
  padding-top: 60px;
  background-color: aliceblue;
}
</style>
