<template>
  <div>
    <h1 class="text-primary">Work History</h1>
    <div class="m-3 mb-5">
      <work-history-entry v-for="job in jobs" :key="job.name" :job="job"/>
    </div>
  </div>
</template>

<script>
import WorkHistoryEntry from "@/components/WorkHistory/WorkHistoryEntry";

export default {
  name: "WorkHistory",
  components: {WorkHistoryEntry},
  data() {
    return {
      jobs: [
        {
          name: "GDIT",
          description: "Contractor for the EPA through General Dynamics Information Technology.",
          bullets: [
            "Worked with tools including: Django, Flask, Javascript, VueJS, Elasticsearch/ELK, MySQL, PostgreSQL, Docker, Docker-Compose, JsonApi.",
            "Took an active part in the Agile lifecycle of a project as a developer. Duties including: Daily Scrum, Pointing/Grooming of User Stories, Sprint Retrospectives and Planning.",
            "Coded and reviewed both front-end, back-end, and dev-ops user stories to the requested acceptance criteria. Requested guidance from PO when requests were unclear."
          ],
          startDate: "November 2019",
          endDate: "Present",
          url: "https://www.gdit.com/"
        },
        {
          name: "CastleBranch",
          description: "Developer working on client-focused background check Web Applications",
          bullets: [
            "Develop code for LAMP and LAPP stack web applications.",
            "Code within the Laravel framework as well as frameworkless legacy PHP.",
            "Follow established design patterns such as MVC, Eloquent, CRUD REST/API.",
            "Adapt to working on new code bases with minimal guidance.",
            "Fix code and data bugs both on the front and back end."
          ],
          startDate: "March 2017",
          endDate: "November 2019",
          url: "https://discover.castlebranch.com/"
        },
      ]
    }
  }
}
</script>

<style scoped>

</style>