<template>
  <MyHeaderAboutVue />
  <MyResumeVue />
  <MySkillsVue />
  <MyProjectsVue />
</template>

<script>
import MyResumeVue from './about_me/MyResume.vue';
import MySkillsVue from './about_me/MySkills.vue';
import MyHeaderAboutVue from './about_me/MyHeaderAbout.vue';
import MyProjectsVue from './about_me/MyProjects.vue';

export default {
  components: {
    MySkillsVue,
    MyResumeVue,
    MyHeaderAboutVue,
    MyProjectsVue
  }
}
</script>

<style>
.titles {
  color: #b6b6b6;
  font-size: 1.4em;
  display: flex;
  margin-bottom: 30px;
}
</style>