<template>
  <div class="hero">
    <div class="text-container">
      <div class="text">
        <h1>What's <span>Poppin</span></h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.hero {
  background-image: url('../assets/img/hero-background.jpg');
  background-size: cover;
  width: 100vw;
  height: 500px;
  /* filter: brightness(50%); */
  /* max-height: 500px; */
}

.text-container {
  z-index: 99;
  /* position: absolute; */
  top: 0;
  margin: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.text {
  padding: 0 16px;
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
}
h1 {
  color: #fff;
  font-weight: 700;
  font-size: 5rem;
}

h1 span {
  font-weight: 900;
  color: var(--emphasys);
}
</style>
