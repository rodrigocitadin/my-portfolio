<template>
  <button class="button" v-for="button in buttons" :key="button.id" target="_blank">
    <a :href="button.link">{{ button.msg }}</a>
  </button>
</template>

<script>
export default {
  data() {
    return {
      buttons: [
        {
          id: 1,
          msg: 'ABOUT ME',
          link: '',
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
        },
        {
          id: 4,
          msg: 'DEV.TO',
          link: 'https://dev.to/rodrigocitadin',
        }
      ]
    }
  }
}
</script>

<style>
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