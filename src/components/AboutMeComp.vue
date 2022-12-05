<template>
  <img class="x-icon" src="@/assets/images/x-icon.png" @click="onClickShowAbout()" />
  <HeaderComp />
  <ResumeComp />
  <SkillsComp />
  <ProjectsComp />
</template>

<script>
import ResumeComp from '@/components/about_me/ResumeComp.vue';
import SkillsComp from '@/components/about_me/SkillsComp.vue';
import HeaderComp from '@/components/HeaderComp.vue';
import ProjectsComp from '@/components/about_me/ProjectsComp.vue';

export default {
  components: {
    SkillsComp,
    ResumeComp,
    HeaderComp,
    ProjectsComp
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