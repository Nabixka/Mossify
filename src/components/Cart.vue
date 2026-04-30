<script setup>
    import { Icon } from '@iconify/vue';
</script>

<template>
  <div class="px-4 pt-6 pb-35 flex flex-col gap-4">

    <!-- Title -->
    <h1 class="font-serif text-2xl text-green-950 font-bold">Keranjang</h1>

    <!-- Opsi -->
    <div class="flex justify-between items-center">
      <h5 class="text-sm text-gray-500">3 Produk</h5>
      <button class="flex items-center gap-2 text-sm text-red-500 hover:text-red-600">
        Hapus Semua 
        <Icon icon="tabler:trash" width="18" height="18" />
      </button>
    </div>

    <!-- List Item -->
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-4">

      <!-- Item -->
      <div class="bg-white rounded-2xl p-3 flex gap-3 shadow-sm">

        <!-- Gambar -->
        <img src="/src/assets/kokedama.jpg" 
             class="w-24 h-24 object-cover rounded-xl">

        <!-- Detail -->
        <div class="flex flex-col justify-between w-full">

          <div>
            <h3 class="text-sm font-medium text-gray-800">
              Kokedama Sirih Gading
            </h3>
            <h3 class="text-green-900 font-bold text-sm mt-1">
              Rp85.000
            </h3>
          </div>

          <!-- Quantity -->
          <div class="flex items-center justify-between mt-2">
            
            <div class="flex items-center border border-gray-300 rounded-lg overflow-hidden">
              <button class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="lucide:minus" width="16" height="16" />
              </button>

              <input type="text" value="1" class="w-10 text-center text-sm outline-none">

              <button class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="ic:twotone-plus" width="16" height="16" />
              </button>
            </div>

            <!-- Optional delete per item -->
            <button class="text-gray-400 hover:text-red-500">
              <Icon icon="mdi:trash-outline" width="18" height="18" />
            </button>

          </div>

        </div>
      </div>

      <!-- Copy item (biar konsisten) -->
      <div class="bg-white rounded-2xl p-3 flex gap-3 shadow-sm">
        <img src="/src/assets/kokedama.jpg" class="w-24 h-24 object-cover rounded-xl">
        <div class="flex flex-col justify-between w-full">
          <div>
            <h3 class="text-sm font-medium text-gray-800">Kokedama Sirih Gading</h3>
            <h3 class="text-green-900 font-bold text-sm mt-1">Rp85.000</h3>
          </div>
          <div class="flex items-center justify-between mt-2">
            <div class="flex items-center border border-gray-300 rounded-lg overflow-hidden">
              <button class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="lucide:minus" width="16" height="16" />
              </button>
              <input type="text" value="1" class="w-10 text-center text-sm outline-none">
              <button class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="ic:twotone-plus" width="16" height="16" />
              </button>
            </div>
            <button class="text-gray-400 hover:text-red-500">
              <Icon icon="mdi:trash-outline" width="18" height="18" />
            </button>
          </div>
        </div>
      </div>

    </div>

    <!-- Ringkasan -->
    <div class="bg-white rounded-2xl p-4 shadow-sm mt-4 flex flex-col gap-3">

      <h2 class="font-serif text-green-950 font-bold">
        Ringkasan Belanja
      </h2>

      <div class="flex justify-between text-sm text-gray-600 border-b pb-2">
        <span>Subtotal (3 Produk)</span>
        <span>Rp265.000</span>
      </div>

      <div class="flex justify-between font-bold text-green-900">
        <span>Total</span>
        <span>Rp265.000</span>
      </div>

    </div>

    <!-- Action -->
    <div class="fixed bottom-0 left-0 w-full bg-white border-t p-4 grid grid-cols-1 lg:grid-cols-2 gap-2">

      <button class="rounded-xl font-semibold bg-green-950 text-white py-3 hover:bg-green-800 transition">
        Checkout
      </button>

      <button class="border border-green-950 text-green-950 font-semibold rounded-xl py-3 hover:bg-green-50 transition">
        Lanjut Belanja
      </button>

    </div>

  </div>
</template>