<template>
  <div class="container">
    <h3 class="titles align-center">Projects</h3>

    <div v-for="project in projects" :key="project.id">
      <h4 class="project-title">{{ project.name }}</h4>
      <div class="projects">
        <div class="img-center">
          <img class="project-img" :src="project.photo" alt="Project photo">
        </div>

        <p class="text">{{ project.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
let projects = require('@/assets/jsons/projects.json');

export default {
  data() {
    return {
      projects
    }
  },
}
</script>

<style>
.project-title {
  color: whitesmoke;
  font-size: 1.6em;
  margin-bottom: 10px;
  margin-top: 60px;
}

.project-img {
  width: 100%;
  max-width: 320px;
  max-height: 320px;
  margin-bottom: 40px;
}

.img-center {
  display: flex;
  justify-content: center;
}

@media (min-width: 900px) {
  .projects {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .project-img {
    width: 320px;
    height: 320px;
    margin-bottom: 40px;
    margin-right: 40px;
  }
}
</style>