<template>
  <b-container>
    <b-row>
      <b-col cols="5">
        <sidebar />
      </b-col>
      <b-col>
        <h1 class="text-primary">
          Michael Barbour
        </h1>
        <div class="m-3 mb-5">
          <span>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas semper ut quam vitae pulvinar. Praesent
            vel ipsum tortor. Nullam turpis tortor, gravida vitae quam ac, accumsan commodo nisi. Nullam tortor sem,
            consequat ac finibus sit amet, mattis rhoncus erat. Nam ac bibendum arcu, et auctor dolor. Curabitur
            dictum tellus sed ipsum iaculis viverra. Nulla cursus nulla vel nisi volutpat, quis semper purus maximus.
            Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nulla
            viverra fermentum sem. Nulla quis tortor sollicitudin, condimentum orci mollis, sagittis mauris. Aenean
            ante nisl, facilisis rhoncus porta imperdiet, ultricies in ipsum. Integer consequat purus et ipsum
            tincidunt, quis bibendum lacus mattis. Nunc eu urna id massa lacinia pellentesque et eu ex. Vestibulum leo
            turpis, tincidunt at luctus eu, accumsan et est. Nulla ligula odio, consequat at tempus ac, accumsan id
            lacus. Mauris suscipit ultricies arcu.
          </span>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Sidebar from "@/components/Sidebar";
export default {
  name: "Profile",
  components: {Sidebar}
}
</script>

<style scoped>

</style>