<template>
  <MyHeaderAboutVue />
  <MyResumeVue />
  <MySkillsVue />
</template>

<script>
import MyResumeVue from './about_me/MyResume.vue';
import MySkillsVue from './about_me/MySkills.vue';
import MyHeaderAboutVue from './about_me/MyHeaderAbout.vue';

export default {
  components: {
    MySkillsVue,
    MyResumeVue,
    MyHeaderAboutVue
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

.container {
  width: 80%;
  max-width: 800px;
  margin: 20px auto;
}
</style>