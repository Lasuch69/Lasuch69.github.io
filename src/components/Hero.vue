<script setup>
</script>

<template>
  <section>
    <div>
      <h1>Hello</h1>
      <h2>I am Lasuch</h2>
      <h3>Self-taught programmer based in Poland.</h3>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url('../assets/untitled.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

div {
  text-align: center;
  display: grid;
  gap: 1.25rem;
  padding: auto 1.25rem;
  margin: 3rem auto;
}

h1 {
  font-size: 6rem;
  color: white;
  font-weight: 700;
}

h2 {
  font-size: 3rem;
  color: white;
}

@media only screen and (max-width: 600px) {
  h1 {
    font-size: 5rem;
  }

  h2 {
    font-size: 2.5rem;
  }
}
</style>
