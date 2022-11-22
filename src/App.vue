<template>
  <MyHeaderVue />
  <div class="buttons">
    <button class="button" v-for="button in buttons" :key="button.id" target="_blank">
      <a :href="button.link">{{ button.msg }}</a>
    </button>
  </div>
</template>

<script>
import MyHeaderVue from './components/MyHeader.vue';

export default {
  name: 'App',
  components: {
    MyHeaderVue
  },
  data() {
    return {
      buttons: [
        {
          id: 1,
          msg: 'ABOUT ME',
          link: '',
          color: '#adadad'
        },
        {
          id: 2,
          msg: 'LINKEDIN',
          link: 'https://www.linkedin.com/in/rodrigobcitadin/',
          color: '#01649b'
        },
        {
          id: 3,
          msg: 'GITHUB',
          link: 'https://github.com/rodrigocitadin',
          color: '#6d2a89'
        },
        {
          id: 4,
          msg: 'DEV.TO',
          link: 'https://dev.to/rodrigocitadin',
          color: '#3ec9b4'
        }
      ]
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

.buttons {
  display: flex;
  flex-direction: column;
}

.button {
  width: 30rem;
  height: 4rem;
  margin: 0.6rem auto;
  border-radius: 12px;
  background-color: whitesmoke;
  -webkit-transition: all 0.3s 0s ease-in;
  -moz-transition: all 0.3s 0s ease-in;
  -o-transition: all 0.3s 0s ease-in;
  transition: all 0.3s 0s ease-in;
}

.button:hover {
  padding-left: 20px;
  background-color: rgb(189, 189, 189);
}

.button a {
  font-size: 1.2rem;
}
</style>
