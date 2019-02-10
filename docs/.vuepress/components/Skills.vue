<template>
  <div>
    <div class="skills">
      <div class="skill">
        <h3>Programming</h3>
        <ul>
          <li v-for="language in languages">
            {{ language.name }} -
            <small>{{ language.time }}</small>
          </li>
        </ul>
      </div>
      <div class="skill">
        <h3>Technologies</h3>
        <ul>
          <li v-for="tech in technologies">
            {{ tech.name }} -
            <small>{{ tech.time }}</small>
          </li>
        </ul>
      </div>
      <div class="skill">
        <h3>Databases</h3>
        <ul>
          <li v-for="database in databases">
            {{ database.name }} -
            <small>{{ database.time }}</small>
          </li>
        </ul>
      </div>
      <div class="skill">
        <h3>Languages</h3>
        <ul>
          <li v-for="tongue in tongues">
            {{ tongue.name }} -
            <small>{{ tongue.level }}</small>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    technologies() {
      const { technologies } = this.$page.frontmatter.skills;
      return technologies;
    },
    languages() {
      const { languages } = this.$page.frontmatter.skills;
      return languages;
    },
    databases() {
      const { databases } = this.$page.frontmatter.skills;
      return databases;
    },
    tongues() {
      const { tongues } = this.$page.frontmatter.skills;
      return tongues;
    }
  }
};
</script>

<style>
.skills {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 10px;
  justify-items: center;
}
.skill {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 2fr;
  width: 100%;
}
.skill ul {
  margin: 0;
}
.skill li {
  white-space: nowrap;
}
.skill h3 {
  margin-bottom: 0;
}
</style>