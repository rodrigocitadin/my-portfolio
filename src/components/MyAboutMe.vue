<template>
  <img class="x-icon" src="@/assets/images/x-icon.png" @click="onClickShowAbout()" />
  <MyHeaderAboutVue />
  <MyResumeVue />
  <MySkillsVue />
  <MyProjectsVue />
</template>

<script>
import MyResumeVue from '@/components/about_me/MyResume.vue';
import MySkillsVue from '@/components/about_me/MySkills.vue';
import MyHeaderAboutVue from '@/components/about_me/MyHeaderAbout.vue';
import MyProjectsVue from '@/components/about_me/MyProjects.vue';

export default {
  components: {
    MySkillsVue,
    MyResumeVue,
    MyHeaderAboutVue,
    MyProjectsVue
  },
  methods: {
    onClickShowAbout() {
      this.$emit('show');
    }
  }
}
</script>

<style>
.x-icon {
  border-radius: 100%;
  width: 40px;
  z-index: 1;
  position: fixed;
  top: 10px;
  left: 10px;
  cursor: pointer;
}

.titles {
  color: #b6b6b6;
  font-size: 1.4em;
  display: flex;
  margin-bottom: 30px;
}
</style>