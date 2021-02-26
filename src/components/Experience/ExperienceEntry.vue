<template>
  <li class="timeline-item bg-white rounded ml-3 p-4 shadow">
    <div class="timeline-arrow"></div>
    <p v-if="entry.startDate && entry.endDate">{{ entry.startDate }} - {{ entry.endDate }}</p>
    <p v-else>{{ entry.endDate }}</p>
    <h2>{{ entry.name }} <a :href="entry.url" target="_blank">
      <b-icon icon="link45deg"/>
    </a></h2>
    <p v-if="entry.bullets">{{ entry.description }}</p>
    <span v-else>{{ entry.description }}</span>
    <ul v-if="entry.bullets" >
      <li v-for="bullet in entry.bullets" :key="bullet">
        {{ bullet }}
      </li>
    </ul>
  </li>
</template>

<script>

export default {
  name: "ExperienceEntry",
  props: ["entry"]
}
</script>

<style scoped>

li.timeline-item {
    margin: 20px 0;
}

/* Timeline item arrow */
.timeline-arrow {
    border-top: 0.5rem solid transparent;
    border-right: 0.5rem solid #fff;
    border-bottom: 0.5rem solid transparent;
    display: block;
    position: absolute;
    left: 2rem;
}

/* Timeline item circle marker */
li.timeline-item::before {
    content: ' ';
    background: #ddd;
    display: inline-block;
    position: absolute;
    border-radius: 50%;
    border: 3px solid #fff;
    left: 11px;
    width: 14px;
    height: 14px;
    z-index: 400;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
}

</style>