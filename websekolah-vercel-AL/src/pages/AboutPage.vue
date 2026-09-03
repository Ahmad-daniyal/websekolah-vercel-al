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
  <main class="max-w-[1200px] mx-auto p-8">
    <div class="flex items-center justify-center pt-5 mb-5 rounded-[50px] text-white bg-gradient-to-r from-blue-600 to-slate-500">
      <h1 class="mb-8">About Page</h1>
    </div>

    <section class="flex items-center gap-8 mb-8">
      <div class="flex-1">
        <h2 class="mb-4">Cerita Kami</h2>
        <p>
          Kami memulai toko ini pada tahun 2018 dengan satu tujuan sederhana:
          menghadirkan produk berkualitas dengan harga yang terjangkau bagi semua orang.
        </p>
        <p>
          Kini kami telah melayani ribuan pelanggan di seluruh Indonesia dan terus
          bertumbuh bersama komunitas kami.
        </p>
      </div>
      <div class="flex-1 h-[300px] rounded-lg bg-slate-400 overflow-hidden" aria-label="Placeholder gambar toko"><img :src="imagePath('2')" alt="Budi Santoso"></div>
      <div class="flex-1 h-[300px] rounded-lg bg-slate-400 overflow-hidden" aria-label="Placeholder gambar toko"><img :src="imagePath('images')" alt="Siti Rahayu"></div>
      <div class="flex-1 h-[300px] rounded-lg bg-slate-400 overflow-hidden" aria-label="Placeholder gambar toko"><img :src="imagePath('3')" alt="Agus Wijaya"></div>
    </section>

    <section>
      <h2 class="mb-4">Tim Kami</h2>
      <div class="flex flex-wrap gap-4">
        <TeamCard
          v-for="member in team"
          :key="member.name"
          :member="member"
          class="grow basis-[220px] max-w-[280px]"
        />
      </div>
    </section>
  </main>
</template>
