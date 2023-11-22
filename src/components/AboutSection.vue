<template>
  <section>
    <h1>About Me</h1>
    <div class="container">
      <div class="element">
        <h2>Background</h2>
        <div class="line"></div>
        <p>My journey with programming started as a small hobby when I was 14 years old. It took off with C++, and game
          development in Unity and Unreal Engine. All this time I wanted to create desktop apps and games. Always
          fascinating
          was how the software we use everyday is made, that’s why my main interest were low-level languages such as
          C++, C and Rust. Recently because of personal reasons I decided to start working on front-end (and certainly
          expand
          to back-end).</p>
      </div>
      <div class="element">
        <h2>Goals</h2>
        <div class="line"></div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt ratione accusamus optio, quia error
          reprehenderit laudantium voluptate voluptatem repellendus reiciendis quae, illo ducimus veritatis maiores
          inventore? Nesciunt, numquam illum! Nemo!</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  padding: 3rem 1.25rem;
  text-align: center;
  background-color: #212121;
}

.container {
  display: grid;
  column-gap: 3rem;
  grid-template-columns: repeat(2, 1fr);
}

.element {
  height: 100%;
  border-radius: 0.5rem;
  border: 0.1rem solid gray;
  padding: 1.5rem;
  margin-top: 2rem;
}

.line {
  width: 100%;
  padding: 0;
  margin: 0;
  border-bottom: 1px solid gray;
  margin-bottom: 1.5rem;
}

h1 {
  color: white;
  font-size: 3rem;
  font-weight: 700;
}

h2 {
  color: white;
  margin-bottom: 1.5rem;
  text-align: center;
}

p {
  margin: auto 1rem;
}


@media only screen and (max-width: 600px) {
  .container {
    grid-template-columns: 1fr;
    row-gap: 2rem;
  }
}
</style>
