<template>
  <div class="align-center">
    <button class="button" @click="onClickShowAbout()">ABOUT ME</button>
    <a class="button" v-for="button in buttons" :key="button.id" :href="button.link" :target="button.target">
      {{ button.msg }}
    </a>
  </div>
</template>

<script>
let buttons = require('@/assets/jsons/buttons.json')

export default {
  data() {
    return { buttons }
  },
  methods: {
    onClickShowAbout() {
      this.$emit('show');
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
  background-color: transparent;
  border: 1px solid whitesmoke;
  font-size: 1.4rem;
  color: whitesmoke;
  cursor: pointer;

  -webkit-transition: all 0.3s 0s ease-in;
  -moz-transition: all 0.3s 0s ease-in;
  -o-transition: all 0.3s 0s ease-in;
  transition: all 0.3s 0s ease-in;
}

.button:hover {
  padding-left: 1.25rem;
  background-color: #161616;
}

a {
  display: flex;
  align-items: center;
  justify-content: center;
}

@media (max-width: 600px) {
  .button {
    width: 20rem;
    height: 3.5rem;
  }
}
</style>