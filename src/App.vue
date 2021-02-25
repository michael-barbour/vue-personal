<template>
  <div id="app" class="container-fluid">
    <b-row>
      <b-col cols="12" md="3">
        <div class="bd-sidebar px-5 mb-5">
          <b-img src="@/assets/headshot.png" fluid rounded="" />
          <dl class="text-left">
            <dt>Age</dt>
            <dd>{{ age }}</dd>

            <dt>Location</dt>
            <dd>Durham, North Carolina</dd>

            <dt>Email</dt>
            <dd>michaelbarbour163@gmail.com</dd>

            <dt>Phone</dt>
            <dd>(919) 559-2676</dd>
          </dl>
        </div>
      </b-col>
      <b-col class="text-left">
        <h1 class="text-primary">Michael Barbour</h1>
        <div class="m-5">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas semper ut quam vitae pulvinar. Praesent
            vel ipsum tortor. Nullam turpis tortor, gravida vitae quam ac, accumsan commodo nisi. Nullam tortor sem,
            consequat ac finibus sit amet, mattis rhoncus erat. Nam ac bibendum arcu, et auctor dolor. Curabitur
            dictum tellus sed ipsum iaculis viverra. Nulla cursus nulla vel nisi volutpat, quis semper purus maximus.
            Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nulla
            viverra fermentum sem. Nulla quis tortor sollicitudin, condimentum orci mollis, sagittis mauris. Aenean
            ante nisl, facilisis rhoncus porta imperdiet, ultricies in ipsum. Integer consequat purus et ipsum
            tincidunt, quis bibendum lacus mattis. Nunc eu urna id massa lacinia pellentesque et eu ex. Vestibulum leo
            turpis, tincidunt at luctus eu, accumsan et est. Nulla ligula odio, consequat at tempus ac, accumsan id
            lacus. Mauris suscipit ultricies arcu.
          </p>
          <p>
            Nullam faucibus tempus diam sed mollis. Quisque nec mi dui. Maecenas tortor est, varius id sem non,
            venenatis bibendum ligula. Curabitur sed ullamcorper tellus. Sed id mollis arcu, vitae malesuada tellus.
            Pellentesque ullamcorper neque ut vulputate scelerisque. Nam lacinia magna sed quam lacinia, in lacinia
            augue tristique. Aliquam erat volutpat. Integer pulvinar justo id leo rutrum suscipit. Suspendisse
            sollicitudin, leo in mollis dignissim, tortor nisl efficitur est, id fringilla tortor mi vel tortor. In
            placerat enim sed maximus consequat. Etiam sit amet tortor augue. Donec ante erat, auctor id orci eget,
            fermentum dapibus libero. Phasellus lectus tellus, ullamcorper ut tortor ut, iaculis varius lectus.
          </p>
          <p>
            Vestibulum interdum odio est, in ornare dolor feugiat ut. Mauris eu nisl tortor. Integer porta condimentum
            enim in elementum. Nunc suscipit rutrum dictum. Pellentesque orci nulla, volutpat a elementum eget,
            porttitor ac mi. Suspendisse feugiat sed leo sit amet faucibus. Curabitur quis rhoncus velit.
          </p>
          <p>
            Sed elit orci, bibendum ut lorem sit amet, fermentum egestas ipsum. In aliquet, tortor et luctus varius,
            turpis velit tempor sapien, nec scelerisque massa nulla eget justo. Fusce efficitur quam metus. Quisque
            odio turpis, ornare ac rhoncus ac, vehicula non magna. Nunc vehicula tincidunt dapibus. Aenean at dapibus
            massa. Duis tortor quam, ultrices ut consequat quis, tincidunt at quam. Aliquam condimentum justo vel
            nulla semper, sed gravida ipsum blandit. Maecenas ut nisl varius dui hendrerit vestibulum. Sed maximus mi
            eu aliquam lobortis.
          </p>
          <p>
            Pellentesque sem dolor, vestibulum at purus non, porta sodales nunc. In consectetur finibus tortor, non
            lacinia diam dignissim nec. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac
            turpis egestas. Proin eu velit id orci tincidunt finibus. Maecenas quis justo pretium, euismod quam in,
            placerat purus. Aenean lacinia commodo eros eleifend luctus. Aenean sit amet posuere ligula. Nulla
            facilisi.
          </p>
        </div>
        <h1 class="text-primary"> Work History</h1>
        <div class="m-5">
          <div class="d-flex align-items-center justify-content-between">
            <h2>GDIT</h2>
            <span>November 2019 - Present</span>
          </div>
          <p>Contractor for the EPA through General Dynamics IT.</p>
          <ul>
            <li>Worked with tools including: Django, Flask, Javascript, VueJS, Elasticsearch/ELK, MySQL, PostgreSQL, Docker, Docker-Compose, JsonApi.</li>
            <li>Took an active part in the Agile lifecycle of a project as a developer. Duties including: Daily Scrum, Pointing/Grooming of User Stories, Sprint Retrospectives and Planning.</li>
            <li>Coded and reviewed both front-end, back-end, and dev-ops user stories to the requested acceptance criteria.  Requested guidance from PO when requests were unclear.</li>
          </ul>

          <div class="d-flex align-items-center justify-content-between">
            <h2>CastleBranch</h2>
            <span>March 2017 - November 2019</span>
          </div>
          <p>Contractor for the EPA through General Dynamics IT.</p>
          <ul>
            <li>Worked with tools including: Django, Flask, Javascript, VueJS, Elasticsearch/ELK, MySQL, PostgreSQL, Docker, Docker-Compose, JsonApi.</li>
            <li>Took an active part in the Agile lifecycle of a project as a developer. Duties including: Daily Scrum, Pointing/Grooming of User Stories, Sprint Retrospectives and Planning.</li>
            <li>Coded and reviewed both front-end, back-end, and dev-ops user stories to the requested acceptance criteria.  Requested guidance from PO when requests were unclear.</li>
          </ul>
        </div>
        <h1 class="text-primary">Education</h1>
        <div class="m-5">
          <div class="d-flex align-items-center justify-content-between">
            <h2>University of North Carolina - Wilmington</h2>
            <span>May 2016</span>
          </div>
          <p>Graduated with a Bachelor of Science in computer science</p>
        </div>
        <h1 class="text-primary">Github</h1>
        <div class="m-5">
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  computed: {
    age: function() {
      let now = Date.now()
      let bday = new Date(1992, 11, 18)
      return new Date(now - bday).getFullYear() - 1970
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.bd-sidebar {
  order: 0;
  -ms-flex: 0 1 320px;
  flex: 0 1 320px;
  position: -webkit-sticky;
  position: sticky;
  top: 4rem;
  z-index: 1000;
}
</style>
