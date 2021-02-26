<template>
  <div class="sidebar-cstm mb-5">
    <b-img src="@/assets/headshot.png" fluid rounded="" />
    <dl class="pt-3 text-left">
      <dt>Age</dt>
      <dd>{{ age }}</dd>

      <dt>Location</dt>
      <!--Break on North Carolina-->
      <dd>Durham, <span style="white-space: nowrap">North Carolina</span></dd>

      <dt>Email</dt>
      <dd>
        michaelbarbour163<wbr>@gmail.com
      </dd>

      <dt>Phone</dt>
      <dd>(919) 559-2676</dd>
    </dl>
    <div class="text-left">
      <a class="p-2" href="https://www.github.com/michael-barbour" target="_blank">
        <b-icon icon="github" font-scale="2"/>
      </a>
      <a class="p-2" href="mailto:michaelbarbour163@gmail.com">
        <b-icon icon="mailbox" font-scale="2"/>
      </a>
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
  border-radius: 1rem;
  background-color: var(--light);
  padding: 2rem;
}
</style>