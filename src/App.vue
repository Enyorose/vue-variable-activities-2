<template>
  <div id="app" class="flex justify-center">
    <article class="max-w-sm rounded overflow-hidden shadow-lg mt-4 p-4">
      <!-- replace all text in <strong> with double moustache dynamic variable -->
      <h1 class="text-xl mb-2">
        Hello my name is <strong>{{ users[0].name }}</strong>
      </h1>
      <p class="text-gray-700 text-base">
        I lived in <strong>Brooks</strong> Alberta
      </p>
      <p class="text-gray-700 text-base">
        My favorite genre of books is <strong>fantasy!</strong>
      </p>
    </article>
  </div>
</template>

<script>
import Vue from "vue";
import VueCompositionAPI from "@vue/composition-api";

Vue.use(VueCompositionAPI);

export default {
  setup() {
    const users = [
      {
        name: "Alex",
        place: "Calgary",
      },
      {
        name: "Rolf",
        place: "Calgary",
      },
      {
        name: "Maria",
        place: "Calgary",
      },
      {
        bookGenres: ["fantasy", "mystery", "paranormal", "comedy"],
      },
    ];

    return {
      users,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

