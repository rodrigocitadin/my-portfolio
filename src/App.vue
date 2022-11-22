<template>
  <MyHeaderVue />
  <div class="buttons">
    <MyButtonsVue />
  </div>
</template>

<script>
import MyHeaderVue from './components/MyHeader.vue';
import MyButtonsVue from './components/MyButtons.vue';

export default {
  name: 'App',
  components: {
    MyHeaderVue,
    MyButtonsVue
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

.buttons {
  display: flex;
  flex-direction: column;
}
</style>
