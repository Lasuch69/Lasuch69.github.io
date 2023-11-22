<script setup>
import ResumeItem from '../components/ResumeItem.vue'
import { ref } from 'vue';

const achievements = ref([
  { message: "Responsive Web Design Certificate", link: "https://www.freecodecamp.org/certification/Lasuch/responsive-web-design" },
  { message: "JavaScript Algorithms and Data Structures Certificate", link: "https://www.freecodecamp.org/certification/Lasuch/javascript-algorithms-and-data-structures" },
]);

const language_skills = ref([
  { message: "Polish (Native)" },
  { message: "English (B2/C1)" },
  { message: "Japanese (N4)" },
]);

const experience = ref([
  { message: "NoiseTexture3D (Godot Engine, C++)", link: "https://github.com/godotengine/godot-proposals/issues/4946" },
  { message: "Vulkan 3D renderer (C++)", link: "https://github.com/Lasuch69/3d-renderer" },
  { message: "Particle simulation (Rust)", link: "https://github.com/Lasuch69/particle-sim" }
]);

const technologies = ref([
  { message: "Linux" },
  { message: "C++ (GCC, 14/17)" },
  { message: "Rust" },
  { message: "HTML" },
  { message: "CSS" },
  { message: "Vue" },
  { message: "Git" },
]);
</script>

<template>
  <div class="container">
    <div class="sidebar">
      <div class="photo-container d-flex">
        <img class="photo" width="128" height="128" src="../assets/avatar.png" alt="">
      </div>
      <div class="contact-container">
        <h2>Contact</h2>
        <div class="phone"></div>
      </div>
    </div>
    <div class="content">
      <div class="name">
        <h1>Lasuch</h1>
        <h2>Self-taught Programmer</h2>
      </div>
      <div class="separator"></div>
      <div class="profile">
        <p>Based In Poland. Since 2019 aspiring to become an expert in software engineering.</p>
        <p>I base my expertise around low-level languages to squize the most performance out of any algorithm.
          That said I am open and willing to learn any technology, to achieve any ambitious goals.
        </p>
        <p>I love free and open source software and contribute regularly to Godot Engine.</p>
      </div>
      <div class="separator"></div>
      <div class="items-container">
        <ResumeItem title="Achievements" icon="https://img.icons8.com/ios/50/goal--v1.png" :items=achievements />
        <ResumeItem title="Experience" icon="https://img.icons8.com/ios/50/light-on--v1.png" :items=experience />
        <ResumeItem title="Language Skills" icon="https://img.icons8.com/ios/50/development-skill.png"
          :items=language_skills />
        <ResumeItem title="Technology" icon="https://img.icons8.com/windows/32/electronics.png" :items=technologies />
      </div>
      <p>Icons by <a href="https://icons8.com">Icons8</a></p>
    </div>
  </div>
</template>

<style scoped>
.items-container * {
  margin-bottom: 1.5rem;
}

h1 {
  font-weight: 300;
  font-size: 3rem;
}

h2 {
  font-size: 1.5rem;
  font-weight: 300;
  color: gray;
  margin-bottom: 1rem;
}

p {
  color: black;
  font-size: 1rem;
}

.items {
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.container {
  min-height: 1200px;
  padding: 0;
  background-color: white;
  box-shadow: 0px 0px 5px black;
  display: grid;
  grid-template-columns: 1fr 4fr;
}

.sidebar {
  background-color: #222;
  height: 100%;
}

.content {
  padding-top: 3rem;
  margin: 0 2.5rem;
}

.photo-container {
  margin-top: 3rem;
}

.photo {
  border-radius: 100%;
  border: solid black 2px;
  border-color: gray;
  margin: 0 auto;
}

.avatar-container {
  width: 100%;
  justify-content: center;
  align-items: center;
  margin-top: 3rem;
}

.contact-container {
  margin-top: 4rem;
  margin-left: 3rem;
}

.name {
  width: 100%;
  color: black;
}

.separator {
  border-top: solid #ddd 1px;
  margin-bottom: 1.5rem;
}

@media only screen and (max-width: 600px) {
  .sidebar {
    display: none;
  }

  .container {
    display: flex;
  }
}
</style>
