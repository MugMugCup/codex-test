<template>
  <div>
    <header class="bg-dark text-white mb-4">
      <nav class="navbar navbar-expand-lg container">
        <a class="navbar-brand" href="#">My Vue Site</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Gallery</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </nav>
    </header>

    <main class="container">
      <div class="text-center mb-5">
        <h1>Welcome to My Site</h1>
        <p class="lead">A simple example using Vue 3 and Bootstrap.</p>
      </div>

      <div class="row g-4">
        <div class="col-md-4" v-for="(card, index) in cards" :key="index">
          <div class="card h-100">
            <img :src="card.img" class="card-img-top" :alt="`Image ${index + 1}`" />
            <div class="card-body">
              <h5 class="card-title">{{ card.title }}</h5>
              <p class="card-text">{{ card.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </main>

    <footer class="bg-light py-4 mt-5">
      <div class="container text-center">
        <span class="text-muted">© 2025 My Vue Site</span>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const cards = ref([
  {
    img: 'https://via.placeholder.com/400x200?text=Image+1',
    title: 'Card 1',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
  },
  {
    img: 'https://via.placeholder.com/400x200?text=Image+2',
    title: 'Card 2',
    text: 'Integer lobortis est id quam consequat, sit amet pretium arcu facilisis.'
  },
  {
    img: 'https://via.placeholder.com/400x200?text=Image+3',
    title: 'Card 3',
    text: 'Fusce placerat lorem sit amet turpis auctor, eu sollicitudin nulla volutpat.'
  }
]);
</script>

<style>
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>
