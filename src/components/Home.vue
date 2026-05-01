<script setup>
import { Icon } from '@iconify/vue'
import { inject, ref } from 'vue'

const { addToCart, goToShop } = inject('cart')

const featuredItems = ref([
//   {
//     nama: 'Kokedama Sirih Gading',
//     harga: 50000,
//     deskripsi: 'Tanaman hijau elegan yang mudah dirawat dan cocok untuk dekorasi rumah.',
//     image: '/sirih_gading.png'
//   }
//   {
//     nama: 'Custom Kokedama',
//     harga: 75000,
//     deskripsi: 'Pesan sesuai model favoritmu dengan kombinasi tanaman dan warna akar sendiri.',
//     custom: true,
//   }
    {
      nama: 'Kokedama Lidah Mertua',
      harga: 50000,
      deskripsi: 'Tanaman yang dapat membersihkan udara dan memberikan sentuhan hijau yang segar di rumahmu.',
      image: '/lidah_mertua.png'
    }
])

const formatRp = (value) => {
  return new Intl.NumberFormat('id-ID', { maximumFractionDigits: 0 }).format(value)
}
</script>

<template>
  <div class="flex flex-col gap-12">

    <!-- HERO -->
    <section class="relative rounded-3xl overflow-hidden bg-gradient-to-r from-green-900 via-green-800 to-emerald-700 py-16 px-6 md:py-24 md:px-12">
      <div class="max-w-2xl">
        <h1 class="font-serif text-5xl md:text-6xl font-bold text-white mb-4">
          Selamat Datang di Mossify
        </h1>
        <p class="text-xl text-green-100 mb-8">
          Temukan keindahan alami dengan koleksi kokedama premium kami.
        </p>
        <button 
          @click="goToShop()" 
          class="bg-white text-green-900 px-8 py-3 rounded-full font-bold text-lg hover:bg-green-50 transition hover:scale-105">
          Mulai Belanja
        </button>
      </div>

      <!-- Decorative Image -->
      <div class="absolute right-0 top-1/2 -translate-y-1/2 opacity-10 pointer-events-none">
        <img src="/kokedama_home.png" class="w-72 md:w-96 object-contain" />
    </div>
    </section>

    <!-- FEATURED -->
    <section>
      <h2 class="font-serif text-4xl font-bold text-green-950 mb-2">Produk Unggulan</h2>
      <p class="text-gray-600 mb-8">Pilihan terbaik kokedama kami</p>

      <div class="grid grid-cols-1 gap-6">
        <div 
          v-for="item in featuredItems" 
          :key="item.nama"
          class="group rounded-3xl overflow-hidden bg-white shadow-md hover:-translate-y-1 hover:shadow-xl transition">

          <div :class="`h-52 bg-gradient-to-br ${item.color} flex h-65 bg-gray-200 items-center justify-center`">
            <img v-if="item.image" :src="item.image" class="w-50 h-60 object-cover bg-gray-200 group-hover:scale-110 transition duration-300">
            <Icon v-else icon="mdi:cog-outline" width="80" class="text-gray-400" />
          </div>

          <div class="p-6">
            <div class="flex flex-col gap-1">
              <h3 class="font-bold text-xl">{{ item.nama }}</h3>
              <span class="text-green-900 font-bold">Rp{{ formatRp(item.harga) }}</span>
            </div>

            <p class="text-sm text-gray-600 mt-3">{{ item.deskripsi }}</p>

            <div class="mt-6">
              <button
                v-if="!item.custom"
                @click="addToCart(item)"
                class="w-full flex items-center justify-center gap-2 bg-emerald-700 text-white py-2 rounded-full hover:bg-emerald-800 transition">
                <Icon icon="mdi:cart-plus" width="18"/>
                Tambah
              </button>

              <button
                v-else
                @click="goToShop()"
                class="w-full flex items-center justify-center gap-2 bg-green-900 text-white py-2 rounded-full hover:bg-green-800 transition">
                <Icon icon="mdi:cog-outline" width="18"/>
                Custom
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- WHY -->
    <section>
      <h2 class="text-center text-4xl font-bold text-green-950 mb-8">Kenapa Mossify?</h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div class="bg-white p-6 rounded-2xl shadow text-center">
          <Icon icon="mdi:leaf" width="32" class="mx-auto text-green-900 mb-3"/>
          <h3 class="font-bold">100% Alami</h3>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow text-center">
          <Icon icon="mdi:hand-heart" width="32" class="mx-auto text-green-900 mb-3"/>
          <h3 class="font-bold">Handmade</h3>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow text-center">
          <Icon icon="mdi:truck-fast" width="32" class="mx-auto text-green-900 mb-3"/>
          <h3 class="font-bold">Cepat</h3>
        </div>

        <div class="bg-white p-6 rounded-2xl shadow text-center">
          <Icon icon="mdi:star" width="32" class="mx-auto text-green-900 mb-3"/>
          <h3 class="font-bold">Kualitas</h3>
        </div>
      </div>
    </section>

    <!-- CARE -->
    <section class="bg-gradient-to-r from-green-50 to-emerald-50 rounded-3xl p-8 md:p-12">
      <div class="grid md:grid-cols-2 gap-8 items-center">

        <!-- TEXT -->
        <div>
          <h2 class="text-4xl font-bold text-green-950 mb-4">
            Tips Merawat Kokedama
          </h2>

          <ul class="space-y-3 text-gray-700">
            <li>✔ Siram 2-3x seminggu</li>
            <li>✔ Cahaya tidak langsung</li>
            <li>✔ Hindari suhu ekstrem</li>
          </ul>
        </div>

        <!-- IMAGE FIX -->
        <div class="bg-white rounded-2xl p-6 shadow-lg">
          <div class="w-full h-100 overflow-hidden rounded-xl">
            <img 
              src="/kokedama_home.png"
              class="w-full h-full object-cover object-center group-hover:scale-105 transition duration-300"
            />
          </div>

          <p class="text-center text-gray-700 font-semibold mt-4">
            Bisa bertahan bertahun-tahun 🌱
          </p>
        </div>

      </div>
    </section>

    <!-- CTA -->
    <section class="text-center py-8">
      <h2 class="text-4xl font-bold text-green-950 mb-4">
        Siap Memperindah Rumahmu?
      </h2>

      <button 
        @click="goToShop()" 
        class="bg-green-900 text-white px-8 py-3 rounded-full hover:bg-green-800 transition">
        Belanja Sekarang
      </button>
    </section>

  </div>
</template>