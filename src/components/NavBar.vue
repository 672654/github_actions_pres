<script setup lang="ts">
import { ref } from 'vue';

const links = ref([
  { name: 'Home', href: '#' },
  { name: 'About', href: '#' },
  { name: 'Contact', href: '#' },
]);

</script>

<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class ="nav-logo">
        <img src = "/icon.png" alt="Logo" width="40" height="40"/>
        <span class="nav-title">MyApp</span>
      </div>
      <ul class="nav-menu">
        <li v-for="link in links" :key="link.name" class="nav-item">
          <a class="nav-link":href="link.href">{{ link.name }}</a>
        </li>
      </ul>
    </div> 
  </nav>
</template>

<style scoped>
.navbar {
  background-color: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
  padding: 1rem 0;
}

.nav-container {
  display: flex;
  justify-content:flex-start;
  align-items:center;
  gap: 500px;
  padding: 0 2rem;
  position: relative;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.5rem;
  font-weight: bold;
  color: #333;
}

.logo-img {
  width: 40px;
  height: 40px;
  object-fit: contain;
}

.logo-text {
  color: #dbab67;
}

.nav-menu {
  display: flex;
  justify-content: center;
  list-style: none;
  gap: 5rem;
  margin: 0;
  padding: 0;
}

.nav-item {
  position: relative;
}

.nav-link {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  font-size: 20px;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.nav-link:hover {
  color: #334f79;
  background-color: rgba(219, 171, 103, 0.1);
}

/* Responsiv design */
@media (max-width: 768px) {
  .nav-menu {
    gap: 1rem;
  }
  
  .nav-link {
    font-size: 0.9rem;
    padding: 0.4rem 0.8rem;
  }
  
  .nav-container {
    padding: 0 1rem;
  }
}
</style>