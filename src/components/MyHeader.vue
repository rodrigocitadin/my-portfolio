<template>
  <header class="header">
    <div class="my-pic">
      <img src="../assets/my-picture.png" alt="Citadin's picture" id="citadin-pic">
    </div>
    <div class="my-name">
      <h1>Citadin</h1>
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
  margin: 80px 0 25px 0;
}

#citadin-pic {
  width: 230px;
  background-color: whitesmoke;
  border-radius: 100%;
}

.my-name {
  color: whitesmoke;
  margin-bottom: 120px;
  display: flex;
  justify-content: center;
}
</style>