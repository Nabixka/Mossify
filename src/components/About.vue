<script setup>
    import { Icon } from '@iconify/vue';
</script>

<template>
  <div class="pb-24">

    <!-- Title -->
    <div class="px-4 pt-6">
      <h1 class="font-serif text-2xl text-green-950 font-bold">
        About Kokedama
      </h1>
      <p class="mt-2 text-gray-600 text-sm">
        Seni tanaman yang membawa keindahan alam lebih dekat denganmu
      </p>
    </div>

    <!-- Pengertian -->
    <div class="bg-white mt-6 mx-4 p-4 rounded-2xl shadow-sm flex gap-4">

      <!-- Text -->
      <div class="flex flex-col gap-2">
        <h3 class="font-serif font-semibold text-lg text-green-950">
          Apa itu Kokedama?
        </h3>
        <p class="text-sm text-gray-600 leading-relaxed">
          Kokedama adalah seni menanam asal Jepang yang menggunakan bola tanah
          yang dibungkus dengan lumut. Tanaman ditanam tanpa pot sehingga
          memberikan kesan alami, minimalis, dan menenangkan.
        </p>
      </div>

      <!-- Image -->
      <img 
        src="/src/assets/kokedama.jpg" 
        class="w-28 h-32 object-cover rounded-xl"
      >
    </div>

    <!-- Keunggulan -->
    <div class="grid grid-cols-2 gap-4 px-4 mt-6">

      <div class="bg-white p-3 rounded-2xl shadow-sm flex flex-col items-center text-center gap-2">
        <Icon icon="meteor-icons:leaf" width="22" height="22" class="text-green-900"/>
        <h3 class="text-green-950 font-semibold text-sm">Alami</h3>
        <p class="text-xs text-gray-500">
          Menggunakan bahan alami dan ramah lingkungan
        </p>
      </div>

      <div class="bg-white p-3 rounded-2xl shadow-sm flex flex-col items-center text-center gap-2">
        <Icon icon="charm:plant-pot" width="22" height="22" class="text-green-900"/>
        <h3 class="text-green-950 font-semibold text-sm">Estetis</h3>
        <p class="text-xs text-gray-500">
          Mempercantik ruangan dengan sentuhan hijau alami
        </p>
      </div>

      <div class="bg-white p-3 rounded-2xl shadow-sm flex flex-col items-center text-center gap-2">
        <Icon icon="boxicons:water-spray" width="22" height="22" class="text-green-900"/>
        <h3 class="text-green-950 font-semibold text-sm">Mudah Dirawat</h3>
        <p class="text-xs text-gray-500">
          Perawatan sederhana dengan penyiraman rutin
        </p>
      </div>

      <div class="bg-white p-3 rounded-2xl shadow-sm flex flex-col items-center text-center gap-2">
        <Icon icon="mdi:present" width="22" height="22" class="text-green-900"/>
        <h3 class="text-green-950 font-semibold text-sm">Hadiah Spesial</h3>
        <p class="text-xs text-gray-500">
          Pilihan unik untuk orang tersayang
        </p>
      </div>

    </div>

    <!-- Manfaat -->
    <div class="px-4 mt-8 flex flex-col gap-3">

      <h3 class="font-serif text-green-950 font-semibold text-lg">
        Manfaat Kokedama
      </h3>

      <div class="flex flex-col gap-2">

        <div class="flex items-center gap-2 text-sm text-gray-700">
          <Icon icon="mingcute:check-fill" width="16" height="16" class="text-green-900"/>
          <span>Membantu menyegarkan udara</span>
        </div>

        <div class="flex items-center gap-2 text-sm text-gray-700">
          <Icon icon="mingcute:check-fill" width="16" height="16" class="text-green-900"/>
          <span>Meningkatkan suasana hati dan mengurangi stres</span>
        </div>

        <div class="flex items-center gap-2 text-sm text-gray-700">
          <Icon icon="mingcute:check-fill" width="16" height="16" class="text-green-900"/>
          <span>Menambah keindahan dekorasi ruangan</span>
        </div>

        <div class="flex items-center gap-2 text-sm text-gray-700">
          <Icon icon="mingcute:check-fill" width="16" height="16" class="text-green-900"/>
          <span>Cocok untuk berbagai tanaman indoor</span>
        </div>

      </div>

    </div>

  </div>
</template>