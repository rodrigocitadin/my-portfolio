<template>
  <div class="align-center">
    <button class="button" v-for="button in buttons" :key="button.id">
      <a :href="button.link" :target="button.target">{{ button.msg }}</a>
    </button>
  </div>
</template>

<script>
let buttons = require('../assets/buttons.json')

export default {
  data() {
    return { buttons }
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

@media (max-width: 600px) {
  .button {
    width: 20rem;
    height: 3.5rem;
  }
}
</style>