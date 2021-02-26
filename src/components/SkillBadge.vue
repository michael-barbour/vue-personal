<template>
  <h4>
    <b-badge :variant="variant">{{ text }}</b-badge>
  </h4>
</template>

<script>
export default {
  name: "SkillBadge",
  props: ["text", "variant"],
  computed: {
    bgcolor: function () {
      return `bg-${this.variant}`
    }
  }
}
</script>

<style scoped>

</style>