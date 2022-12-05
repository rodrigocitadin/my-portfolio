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
html {
  box-sizing: border-box;
  font-size: 16px;
  background: #202020;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

body,
h1,
h2,
h3,
h4,
h5,
h6,
p,
ol,
ul {
  margin: 0;
  padding: 0;
  font-weight: normal;
}

ol,
ul {
  list-style: none;
}

img {
  max-width: 100%;
  height: auto;
}

a {
  color: black;
  text-decoration: none;
}

button {
  border: none;
}

* {
  font-family: 'JetBrains Mono', monospace;
}

.container {
  width: 80%;
  max-width: 800px;
  margin: 20px auto;
}

.align-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
