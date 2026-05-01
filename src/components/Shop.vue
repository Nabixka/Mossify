<script setup>
    import { onMounted, ref, inject } from 'vue';
    import { Icon } from '@iconify/vue';

    const { addToCart } = inject('cart')

    const item = ref([
      {
        "nama" : "Kokedama Lidah Mertua",
        "harga" : 70000,
        "image" : "/lidah_mertua.png"
      },
      {
        "nama" : "Kokedama Sirih Gading Hijau/Lemon",
        "harga" : 30000,
        "image" : "/sirih_gading.png"
      },
      {
        "nama" : "Kokedama Sirih Gading Variegata",
        "harga" : 40000,
        "image" : "/sirih_gading_variegeta.png"
      },
      {
        "nama" : "Kokedama Lili Paris",
        "harga" : 30000,
        "image" : "/lili_paris.png"
      }
    ])

  const goToWA = () => {
    const pesan = encodeURIComponent('Halo Saya Te')
    window.open('https://wa.me/6289618324030?text', '_blank')
  }

  const formatRp = (value) => {
    return new Intl.NumberFormat('id-ID', { maximumFractionDigits: 0 }).format(value)
  }

</script>

<template>
  <div class="flex flex-col gap-2 px-5">
    <!-- Header -->
    <h1 class="font-serif text-3xl text-green-950 font-bold">Shop</h1>
    <h3 class="text-gray-500">Temukan kokedama favoritmu di sini</h3>

    <!-- Grid -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 pt-8">
      
      <!-- Card -->
      <div v-for="i in item" class="bg-whiterounded-2xl lg:w-full w-full shadow-sm hover:shadow-md transition duration-300">
        <div class="flex justify-center bg-gray-200">
          <img :src="i.image" class="bg-gray-200 h-60 w-1/2 object-cover object-center">
        </div>

        <div class="p-3">
          <h4 class="text-sm font-medium text-gray-800">{{ i.nama }}</h4>
          <h4 class="text-green-900 font-bold mt-1">Rp{{ formatRp(i.harga) }}</h4>

          <button @click="addToCart(i)" class="mt-3 w-full bg-green-900 text-white py-1.5 rounded-lg text-sm hover:bg-green-800 transition">
            + Keranjang
          </button>
        </div>
      </div>

    </div>
  </div>
</template>