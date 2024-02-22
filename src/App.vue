<script setup>
import { ref, computed } from "vue";
import Home from "./views/Home.vue";
import Article1 from "./views/Article1.vue";
import Article2 from "./views/Article2.vue";
import Article3 from "./views/Article3.vue";
import Article4 from "./views/Article4.vue";
import Article5 from "./views/Article5.vue";
import NotFound from "./views/NotFound.vue";
import Navbar from "./components/Navbar.vue";
import ContactForm from "./components/ContactForm.vue";

const routes = {
  "/": Home,
  "/article1": Article1,
  "/article2": Article2,
  "/article3": Article3,
  "/article4": Article4,
  "/article5": Article5,
  "/not-found": NotFound,
};

const currentPath = ref(window.location.hash);

window.addEventListener("hashchange", () => {
  currentPath.value = window.location.hash;
});

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || "/not-found"] || NotFound;
});
</script>

<template>
  <Navbar />
  <component :is="currentView" />
  <div>
    <header></header>
    <main></main>
    <aside>
      <contact-form />
    </aside>
  </div>
</template>
