<template>
  <div>
    <div class="d-flex align-items-center justify-content-between flex-wrap mb-3">
      <h2>{{ job.name }} <a :href="job.url" target="_blank">
        <b-icon icon="link45deg"/>
      </a></h2>
      <div>{{ job.startDate }} - {{ job.endDate }}</div>
    </div>
    <p>{{ job.description }}</p>
    <ul>
      <li v-for="bullet in job.bullets" :key="bullet">
        {{ bullet }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: "WorkHistoryEntry",
  props: ["job"]
}
</script>

<style scoped>

</style>