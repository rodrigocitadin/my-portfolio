<template >
  <MyHeaderVue v-if="!showAbout" />
  <MyButtonsVue v-if="!showAbout" @show="onClickShowAbout()" />
  <AboutMeVue v-else @show="onClickShowAbout()" />
</template>

<script>
import MyHeaderVue from '@/components/MyHeader.vue';
import MyButtonsVue from '@/components/MyButtons.vue';
import AboutMeVue from '@/components/MyAboutMe.vue';

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
  methods: {
    onClickShowAbout() {
      this.showAbout = !this.showAbout
    }
  }
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
