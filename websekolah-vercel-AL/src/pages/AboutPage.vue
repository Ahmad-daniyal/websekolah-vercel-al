<script setup>
import TeamCard from '../components/TeamCard.vue'

function imagePath(stem) {
  return `/images/team/${stem}.jpg`
}

const team = [
  { name: 'Budi Santoso', role: 'CEO & Founder' },
  { name: 'Siti Rahayu', role: 'Chief Technology Officer' },
  { name: 'Agus Wijaya', role: 'Head of Marketing' },
  { name: 'Dewi Lestari', role: 'Customer Support Lead' },
]
</script>

<template>
  <main class="about-page">
    <div class="about-header">
      <h1>About Page</h1>
    </div>

    <section class="about-section">
      <div class="about-text">
        <h2>Cerita Kami</h2>
        <p>
          Kami memulai toko ini pada tahun 2018 dengan satu tujuan sederhana:
          menghadirkan produk berkualitas dengan harga yang terjangkau bagi semua orang.
        </p>
        <p>
          Kini kami telah melayani ribuan pelanggan di seluruh Indonesia dan terus
          bertumbuh bersama komunitas kami.
        </p>
      </div>
      <div class="store-image" aria-label="Placeholder gambar toko"><img :src="imagePath('2')" alt="Budi Santoso"></div>
      <div class="store-image" aria-label="Placeholder gambar toko"><img :src="imagePath('images')" alt="Siti Rahayu"></div>
      <div class="store-image" aria-label="Placeholder gambar toko"><img :src="imagePath('3')" alt="Agus Wijaya"></div>
    </section>

    <section class="team-section">
      <h2>Tim Kami</h2>
      <div class="team-list">
        <TeamCard
          v-for="member in team"
          :key="member.name"
          :member="member"
        />
      </div>
    </section>
  </main>
</template>

<style scoped>
.about-page {
  max-width: var(--container-width);
  margin: 0 auto;
  padding: var(--spacing-lg);
}

.about-header {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 1.25rem;
  margin-bottom: 1.25rem;
  border-radius: 50px;
  color: #fff;
  background-image: linear-gradient(
    to right,
    var(--color-primary),
    var(--color-secondary)
  );
}

.about-header h1 {
  margin-bottom: var(--spacing-lg);
}

.about-section {
  display: flex;
  align-items: center;
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-lg);
}

.about-text {
  flex: 1;
}

.about-text p {
  margin-bottom: var(--spacing-md);
}

.about-section h2,
.team-section h2 {
  margin-bottom: var(--spacing-md);
}

.store-image {
  flex: 1;
  height: 300px;
  border-radius: var(--border-radius);
  background-color: var(--color-muted);
  overflow: hidden;
}

.store-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.team-list {
  display: flex;
  flex-wrap: wrap;
  gap: var(--spacing-md);
}

.team-list :deep(.team-card) {
  flex: 1 1 220px;
  max-width: 280px;
}
</style>
