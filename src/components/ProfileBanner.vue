<script setup>
import { ref } from 'vue'

const name = ref('Lasuch')
const login = ref('Lasuch69')
const bio = ref(
  'I enjoy low-level programming, but I like to write some high-level stuff once in a while.'
)
</script>

<template>
  <section class="d-flex">
    <div class="d-grid profile-container">
      <img class="avatar" height="192" width="192" src="../assets/avatar.png" alt="Avatar" />
      <h2>
        {{ name }} <span>@{{ login }}</span>
      </h2>
      <p class="bio">{{ bio }}</p>
      <div class="d-flex wrapper">
        <a class="github-link" href="https://github.com/Lasuch69">My GitHub Profile</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.profile-container {
  gap: 0.5rem;
  padding: 5rem 1.25rem;
}

.avatar {
  border-radius: 100%;
  border: 0.25rem solid gray;
  margin: 0 auto;
}

.wrapper {
  justify-content: center;
}

.bio {
  font-size: 1.25rem;
  font-style: italic;
  color: gray;
  text-align: center;
}

.github-link {
  padding: 0.5rem 1rem;
  background-color: gray;
  text-align: center;
  text-decoration: none;
  color: white;
  border-radius: 0.25rem;
}

.github-link:hover {
  background-color: black;
}

h2 {
  text-align: center;
  color: white;
}

span {
  color: gray;
}

section {
  background-color: black;
  justify-content: center;
  align-items: center;
}
</style>
