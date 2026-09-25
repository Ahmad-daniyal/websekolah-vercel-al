<script setup>
import router from '@/router';


</script>

<template>
  <nav class="navbar">
    <h1>SMK Yadika Soreang</h1>
    <div class="kanan">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/product">Product</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
    </div>
  </nav>
</template>

<style scoped>

.kanan {
  padding: 15px;
}

 h1{color: white;}


.navbar {
  display: flex;
  gap: var(--spacing-lg);
  padding: var(--spacing-md) var(--spacing-lg);
  background-color: var(--color-text);
  justify-content: space-between;

}


.navbar a {
  color: #fff;
  padding: 15px;
}

.navbar a.router-link-active {
  color: var(--color-primary);
}
</style>
