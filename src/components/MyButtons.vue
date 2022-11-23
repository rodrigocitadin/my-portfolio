<template>
  <button class="button align-center" v-for="button in buttons" :key="button.id">
    <a :href="button.link" :target="button.target">{{ button.msg }}</a>
  </button>
</template>

<script>
let buttons = [
  {
    id: 1,
    msg: 'ABOUT ME',
    link: '',
    target: '_self',
  },
  {
    id: 2,
    msg: 'LINKEDIN',
    link: 'https://www.linkedin.com/in/rodrigobcitadin/',
    target: '_blank',
  },
  {
    id: 3,
    msg: 'GITHUB',
    link: 'https://github.com/rodrigocitadin',
    target: '_blank',
  },
  {
    id: 4,
    msg: 'DEV.TO',
    link: 'https://dev.to/rodrigocitadin',
    target: '_blank',
  }
]

export default {
  data() {
    return { buttons }
  }
}
</script>

<style>
.align-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.button {
  width: 30rem;
  height: 4rem;
  margin: 0.6rem auto;
  border-radius: 12px;
  background-color: transparent;
  border: 2px solid whitesmoke;

  -webkit-transition: all 0.3s 0s ease-in;
  -moz-transition: all 0.3s 0s ease-in;
  -o-transition: all 0.3s 0s ease-in;
  transition: all 0.3s 0s ease-in;
}

.button:hover {
  padding-left: 1.25rem;
  background-color: #161616;
}

.button a {
  font-size: 1.4rem;
  color: whitesmoke;
}
</style>