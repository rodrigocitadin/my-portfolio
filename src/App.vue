<template >
  <MyHeaderVue v-if="!showAbout" />
  <button v-if="!showAbout" @click="showAbout = true" class="button align-center">
    <a>ABOUT ME</a>
  </button>
  <MyButtonsVue v-if="!showAbout" />
  <div v-else>
    <img class="x-icon" src="../src/assets/x-icon.png" @click="showAbout = false" />
    <AboutMeVue />
  </div>
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
      showAbout: true
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

.x-icon {
  width: 40px;
  z-index: 1;
  position: fixed;
  top: 10px;
  left: 10px;
}
</style>
