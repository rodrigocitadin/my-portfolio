<template >
  <HeaderComp v-if="!showAbout" />
  <ButtonsComp v-if="!showAbout" @show="onClickShowAbout()" />
  <AboutMeComp v-else @show="onClickShowAbout()" />
</template>

<script>
import HeaderComp from '@/components/HeaderComp.vue';
import ButtonsComp from '@/components/ButtonsComp.vue';
import AboutMeComp from '@/components/AboutMeComp.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    ButtonsComp,
    AboutMeComp,
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
