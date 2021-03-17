<template>
  <li
    class="timeline-item bg-white rounded ml-3 p-4 shadow"
    @click="toggleDetails()"
  >
    <div class="timeline-arrow" />

    <div class="d-flex justify-content-between">
      <h2>
        {{ entry.name }} <a
          :href="entry.url"
          target="_blank"
        >
          <b-icon icon="link45deg" />
        </a>
      </h2>

      <b-icon
        v-if="entry.collapse"
        :icon="visible ? 'chevron-up' : 'chevron-down'"
      />
    </div>

    <h5
      v-if="entry.startDate && entry.endDate"
      class="mb-0"
    >
      {{ entry.startDate }} - {{ entry.endDate }}
    </h5>
    <h5
      v-else
      class="mb-0"
    >
      {{ entry.endDate }}
    </h5>
    <div class="mt-3">
      {{ entry.description }}
    </div>

    <b-collapse
      v-if="entry.collapse"
      v-model="visible"
      class="text-left"
    >
      <div
        v-if="entry.technologies"
        class="my-3"
      >
        <h4>Technologies</h4>
        <div class="d-flex flex-wrap mx-3">
          <skill-badge
            v-for="tech in entry.technologies"
            :key="tech"
            :text="tech"
            variant="secondary"
            class="mx-1"
          />
        </div>
      </div>

      <div
        v-if="entry.bullets"
        class="mt-3"
      >
        <h4>Responsibilities</h4>
        <ul>
          <li
            v-for="bullet in entry.bullets"
            :key="bullet"
          >
            {{ bullet }}
          </li>
        </ul>
      </div>
    </b-collapse>
  </li>
</template>

<script>
import SkillBadge from "@/components/SkillBadge";

export default {
  name: "ExperienceEntry",
  components: {SkillBadge},
  props: {
    "entry": {
      type: Object, default: () => {
        return {}
      }
    }
  },
  data() {
    return {
      visible: false
    }
  },
  methods: {
    toggleDetails: function () {
      this.visible = !this.visible
    }
  }
}
</script>

<style scoped>

li.timeline-item {
  margin: 20px 0;
}

/* Timeline item arrow */
.timeline-arrow {
  border-top: 0.5rem solid transparent;
  border-right: 0.5rem solid var(--secondary);
  border-bottom: 0.5rem solid transparent;
  display: block;
  position: absolute;
  left: 2rem;
}

/* Timeline item circle marker */
li.timeline-item::before {
  content: ' ';
  background: var(--secondary);
  display: inline-block;
  position: absolute;
  border-radius: 50%;
  border: 3px solid #fff;
  left: 11px;
  width: 14px;
  height: 14px;
  z-index: 400;
}

</style>