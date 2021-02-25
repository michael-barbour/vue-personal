<template>
  <div class="sidebar-cstm mb-5">
    <b-img src="@/assets/headshot.png" fluid rounded="" />
    <dl class="pt-3 text-left">
      <dt>Age</dt>
      <dd>{{ age }}</dd>

      <dt>Location</dt>
      <dd>Durham, North Carolina</dd>

      <dt>Email</dt>
      <dd class="d-flex flex-wrap">
        <!--Divs for Word Wrapping-->
        <div>michaelbarbour163</div>
        <div>@gmail.com</div>
      </dd>

      <dt>Phone</dt>
      <dd>(919) 559-2676</dd>
    </dl>
    <div class="text-left">
      <a href="https://www.github.com/michael-barbour" target="_blank"><b-icon icon="github" /></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  computed: {
    age: function () {
      let now = Date.now()
      let bday = new Date(1992, 11, 18)
      return new Date(now - bday).getFullYear() - 1970
    }
  }
}
</script>

<style scoped>
.sidebar-cstm {
  order: 0;
  -ms-flex: 0 1 320px;
  flex: 0 1 320px;
  position: -webkit-sticky;
  position: sticky;
  top: 4rem;
  z-index: 1000;
}
</style>