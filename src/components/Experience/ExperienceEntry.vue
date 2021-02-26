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

    <div v-if="entry.technologies" class="mb-3">
      <h4>Technologies</h4>
      <div class="d-flex flex-wrap mx-3">
        <skill-badge v-for="tech in entry.technologies" :key="tech" :text="tech" variant="primary" class="mx-1" />
      </div>
    </div>

    <div v-if="entry.bullets">
      <h4>Responsibilities</h4>
      <ul>
        <li v-for="bullet in entry.bullets" :key="bullet">
          {{ bullet }}
        </li>
      </ul>
    </div>
  </li>
</template>

<script>
import SkillBadge from "@/components/SkillBadge";

export default {
  name: "ExperienceEntry",
  props: ["entry"],
  components: { SkillBadge }
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
    background: #939393;
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