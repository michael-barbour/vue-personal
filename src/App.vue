<template>
  <b-container id="app">
    <b-row
      class="bg-white p-4"
      style="height: 850px"
    >
      <b-col cols="5">
        <sidebar />
      </b-col>
      <b-col>
        <b-tabs>
          <b-tab
            title="Profile"
            class="p-4"
            active
          >
            <profile />
          </b-tab>
          <b-tab
            title="Experience"
            class="p-4 overflow-auto"
            style="height: 754px"
          >
            <experience />
          </b-tab>
          <b-tab
            title="Projects"
            class="p-4"
          >
            <projects />
          </b-tab>
        </b-tabs>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>

import Profile from "@/components/Profile/Profile";
import Experience from "@/components/Experience/Experience";
import Projects from "@/components/Project/Project";
import Sidebar from "@/components/Sidebar";

export default {
  name: 'App',
  components: {
    Sidebar,
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
