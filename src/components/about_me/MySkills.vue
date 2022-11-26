<template>
  <div v-for="skill in skills" :key="skill.id" class="icons-meters">
    <label class="labels" :for="skill.id"><img class="icons" :src="skill.icon">{{ skill.name
    }}</label>
    <meter :id="skill.id" :value="skill.value" min="0" max="10" low="8" high="8"></meter>
  </div>
</template>

<script>
let skills = require('../../assets/skill.json')

export default {
  data() { return { skills } }
}
</script>

<style>
meter {
  background: lightgrey;
  height: 15px;
}

meter:-moz-meter-optimum::-moz-meter-bar {
  background: indianred;
}

meter:-moz-meter-sub-optimum::-moz-meter-bar {
  background: seagreen;
}

meter:-moz-meter-sub-sub-optimum::-moz-meter-bar {
  background: seagreen;
}
</style>