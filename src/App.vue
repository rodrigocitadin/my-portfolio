<template >
  <MyHeaderVue v-if="!showAbout" />
  <div v-if="!showAbout">
    <MyButtonsVue />
  </div>
  <AboutMeVue v-if="showAbout" />
</template>

<script>
import MyHeaderVue from './components/MyHeader.vue';
import MyButtonsVue from './components/MyButtons.vue';
import AboutMeVue from './components/AboutMe.vue';

export default {
  name: 'App',
  components: {
    MyHeaderVue,
    MyButtonsVue,
    AboutMeVue
  },
  data() {
    return {
      showAbout: false
    }
  },
}
</script>

<style>
* {
  font-family: 'JetBrains Mono', monospace;
}

html {
  height: 100%;
  width: 100%;
  background: #202020;
}
</style>
