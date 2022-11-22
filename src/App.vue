<template>
  <MyPictureVue />
  <div class="my-buttons">
    <a target="_blank" :href="button.link" v-for="button in buttons" :key="button.id">
      <button>{{ button.msg }}</button>
    </a>
  </div>
</template>

<script>
import MyPictureVue from './components/MyPicture.vue';

export default {
  name: 'App',
  components: {
    MyPictureVue
  },
  data() {
    return {
      buttons: [
        {
          id: 1,
          msg: 'ABOUT ME',
          link: ''
        },
        {
          id: 2,
          msg: 'LINKEDIN',
          link: 'https://www.linkedin.com/in/rodrigobcitadin/'
        },
        {
          id: 3,
          msg: 'GITHUB',
          link: 'https://github.com/rodrigocitadin'
        },
        {
          id: 4,
          msg: 'DEV.TO',
          link: 'https://dev.to/rodrigocitadin'
        }
      ]
    }
  },
}
</script>

<style>
html {
  background: #202020;
}

.my-buttons {
  display: flex;
  flex-direction: column;
}
</style>
