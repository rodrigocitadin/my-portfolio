<template>
  <div class="container">
    <div class="my-pic">
      <img class="citadin-pic" src="@/assets/images/my-picture.png" alt="Citadin's picture">
    </div>
    <div class="my-name">
      <h1 class="name animation-typing">Citadin</h1>
      <h2 class="subtitle">Fullstack Developer</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderComp'
}
</script>

<style>
.my-pic {
  text-align: center;
  margin: 2.5rem auto 0;
}

.citadin-pic {
  width: 14.5rem;
  border-radius: 100%;

}

.my-name {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: whitesmoke;
}

.name {
  width: 8.75rem;
  height: 36px;
  margin: 2rem 0 1rem;
  border-right: 3px solid whitesmoke;
  white-space: nowrap;
  overflow: hidden;
}

.animation-typing {
  animation: blinkCursor 1s infinite normal, typing 1s steps(7) 0s normal;
}

.subtitle {
  margin: 0.1rem 0 4rem;
}

@media (max-width: 600px) {
  .citadin-pic {
    width: 10.5rem;
  }

  .my-name {
    margin-bottom: 4rem;
  }

  .subtitle {
    margin: 0.1rem 0 1rem;
  }
}

@keyframes typing {
  from {
    width: 0;
  }

  to {
    width: 8.6rem;
  }
}

@keyframes blinkCursor {
  0% {
    border-right-color: whitesmoke;
  }

  50% {
    border-right-color: transparent;
  }
}
</style>