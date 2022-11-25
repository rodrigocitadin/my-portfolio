<template>
  <div class="my-name name-about">
    <h1 class="name animation-typing">Citadin</h1>
    <h2 class="subtitle">Fullstack Developer</h2>
  </div>

  <h3 class="resume-title">Resume</h3>

  <div class="resume align-center">
    <p class="resume-text">I'm a technology autodidact. I've been studying fullstack development for 1 year. I always
      seek to bring quality
      to
      my applications, with the best methodologies, technologies and metrics, bringing a final product of value and
      maintainability.
    </p>
    <p class="resume-text">
      I'm a functional languages enthusiast. My favorite technologies are Elixir and Rust, but I also have skills in
      Javascript, Typescript, NodeJS, ExpressJS, VueJS, NuxtJS. In databases, I have knowledge in PostgreSQL and
      MongoDB.
    </p>
    <p class="resume-text">
      I'm looking for my first job opportunity. I'm sure I'm prepared for whatever it takes, and if I don't know some
      necessary technology, I can learn easily and quickly.
    </p>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.name-about {
  margin: 80px auto 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.subtitle {
  margin: 10px 0 90px;
}

.resume-title {
  display: flex;
  justify-content: center;
  color: #b6b6b6;
  font-size: 1.4em;
}

.resume {
  width: 80%;
  max-width: 800px;
  margin: 10px auto;
}

.resume-text {
  font-size: 1.2em;
  margin: 20px 0;
  text-align: justify;
  color: whitesmoke;
}
</style>