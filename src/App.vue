<template >
  <MyHeaderVue v-if="!showAbout" />
  <div class="align-center">
    <button v-if="!showAbout" @click="showAbout = true" class="button">
      <a id="about-me">ABOUT ME</a>
    </button>
  </div>
  <MyButtonsVue v-if="!showAbout" />
  <div v-else>
    <img class="x-icon" src="../src/assets/x-icon.png" @click="showAbout = false" />
    <AboutMeVue />
  </div>
</template>

<script>
import MyHeaderVue from './components/MyHeader.vue';
import MyButtonsVue from './components/MyButtons.vue';
import AboutMeVue from './components/MyAboutMe.vue';

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

.x-icon {
  width: 40px;
  z-index: 1;
  position: fixed;
  top: 10px;
  left: 10px;
}

.container {
  width: 80%;
  max-width: 800px;
  margin: 20px auto 60px;
}

.align-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
