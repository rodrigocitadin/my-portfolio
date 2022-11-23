<template >
  <MyHeaderVue v-if="!showAbout" />
  <button v-if="!showAbout" @click="showAbout = true" class="button align-center">
    <a>ABOUT ME</a>
  </button>
  <MyButtonsVue v-if="!showAbout" />
  <AboutMeVue v-else />
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
    AboutMeVue,
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
