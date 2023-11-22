<script setup>
import { ref } from 'vue';

const props = defineProps(["title", "icon", "items"]);

const title = ref(props.title);
const icon = ref(props.icon);
const items = ref(props.items);

let string = "";
console.log(string.length > 0);
</script>

<template>
  <div class="item-container d-flex">
    <div class="side d-flex">
      <img class="icon" width="36" height="36" :src=icon />
      <div class="v-separator"></div>
    </div>
    <div class="main">
      <div class="head">
        <h2>{{ title }}</h2>
        <div class="h-separator"></div>
      </div>
      <div>
        <ul>
          <li v-for="item in items">
            <div class="item-data d-flex">
              <p>{{ item.message }}</p>
              <a class="d-flex" v-if="item.link !== undefined" :href=item.link>
                <img width="25" height="25" src="https://img.icons8.com/ios/50/right--v1.png" alt="right--v1" />
              </a>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.item-data {
  justify-content: space-between;
}

.item-data a {
  margin-right: 0.5rem;
  align-items: center;
}

ul {
  color: black;
  list-style: none;
  margin: 0;
  padding: 0;
}

li {
  padding: 0.25rem;
  padding-left: 1rem;
  font-size: 1rem;
}

li:nth-child(2n) {
  background-color: #ddd;
}

li:last-child {
  border-bottom: solid #ddd 1px;
}

li p {
  margin: 0;
  padding: 0.25rem 0;
  font-size: 1rem;
}

.item-container {
  padding: 0;
}

.side {
  flex-flow: column;
}

.head {
  width: 100%;
}

.head h2 {
  font-weight: 300;
  font-size: 1.5rem;
  color: black;
}


.icon {
  border-radius: 100%;
  background-color: white;
  border: solid black 1px;
  padding: 0.25rem;
}

.main {
  width: 100%;
  margin-left: 1rem;
}

.h-separator {
  border-top: solid #ddd 1px;
  margin: 0;
}

.v-separator {
  border-right: solid black 1px;
  height: 100%;
  width: 50%;
}
</style>
