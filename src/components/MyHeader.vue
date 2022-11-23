<template>
  <header class="header">
    <div class="my-pic">
      <img src="../assets/my-picture.png" alt="Citadin's picture" id="citadin-pic">
    </div>
    <div class="my-name">
      <h1 class="name animation-typing">Citadin</h1>
    </div>
  </header>
</template>

<script>
export default {

}
</script>

<style>
.my-pic {
  display: flex;
  justify-content: center;
  margin: 5rem 0 1.5rem 0;
}

#citadin-pic {
  width: 14.5rem;
  background-color: whitesmoke;
  border-radius: 100%;
}

.my-name {
  color: whitesmoke;
  margin-bottom: 7.5rem;
  display: flex;
  justify-content: center;
}

.name {
  width: 8.75rem;
  border-right: 3px solid whitesmoke;
  white-space: nowrap;
  overflow: hidden;
}

.animation-typing {
  animation: blinkCursor 1s infinite normal, typing 1s steps(7) 0s normal;
}

@keyframes typing {
  from {
    width: 0;
  }

  to {
    width: 8.75rem;
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