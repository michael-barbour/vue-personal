<template>
  <div class="mb-5">
    <b-img
      src="@/assets/headshot.png"
      fluid
    />
    <dl class="pt-3 text-left text-break">
      <dt>Location</dt>
      <!--Break on North Carolina-->
      <dd>Durham, <wbr>North Carolina</dd>

      <dt>Email</dt>
      <dd>
        michaelbarbour163<wbr>@gmail.com
      </dd>

      <dt>Phone</dt>
      <dd>(919) 559-2676</dd>
    </dl>
    <div class="text-left">
      <a
        class="p-2"
        href="https://www.github.com/michael-barbour"
        target="_blank"
      >
        <b-icon
          icon="github"
          font-scale="2"
        />
      </a>
      <a
        class="p-2"
        href="mailto:michaelbarbour163@gmail.com"
      >
        <b-icon
          icon="envelope"
          font-scale="2"
        />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
}
</script>

<style scoped>
/* disabled - to be removed
 * opting out of the sidebar and adding content to the first panel.
 */

/*.sidebar-cstm {*/
/*  order: 0;*/
/*  -ms-flex: 0 1 320px;*/
/*  flex: 0 1 320px;*/
/*  position: -webkit-sticky;*/
/*  position: sticky;*/
/*  top: 40px;*/
/*  z-index: 1000;*/
/*  background-color: var(--light);*/
/*  padding: 2rem;*/
/*}*/
</style>