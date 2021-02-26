<template>
  <div>
    <h1 class="text-primary">Experience</h1>
    <ul class="mb-5 timeline">
      <experience-entry v-for="entry in experiences" :key="entry.name" :entry="entry"/>
    </ul>
  </div>
</template>

<script>
import ExperienceEntry from "@/components/Experience/ExperienceEntry";

export default {
  name: "Experience",
  components: { ExperienceEntry },
  data() {
    return {
      experiences: [
        {
          name: "GDIT",
          description: "Contractor for the EPA through General Dynamics Information Technology.",
          technologies: [
            "django",
            "flask",
            "python",
            "docker",
            "docker-compose",
            "vue",
            "javascript",
            "postgres",
            "mysql",
            "elasticsearch",
            "git"
          ],
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
        {
          name: "University of North Carolina - Wilmington",
          description: "Bachelor of Science in Computer Science",
          endDate: "Graduated May 2016",
          url: "https://uncw.edu"
        },
      ]
    }
  }
}
</script>

<style scoped>

/*
*
* ==========================================
* CUSTOM UTIL CLASSES
* ==========================================
*
*/

/* Timeline holder */
ul.timeline {
    list-style-type: none;
    position: relative;
    padding-left: 1.5rem;
}

 /* Timeline vertical line */
ul.timeline:before {
    content: ' ';
    background: var(--secondary);
    display: inline-block;
    position: absolute;
    left: 16px;
    width: 4px;
    height: 100%;
    z-index: 400;
    border-radius: 1rem;
}

</style>