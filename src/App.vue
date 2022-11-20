<template>
  <MyPictureVue />
  <MyButtonsVue />
</template>

<script>
import MyPictureVue from './components/MyPicture.vue';
import MyButtonsVue from './components/MyButtons.vue';

export default {
  name: 'App',
  components: {
    MyPictureVue,
    MyButtonsVue
  }
}
</script>

<style>
html {
  background: #202020;
}
</style>
