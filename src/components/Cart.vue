<script setup>
    import { Icon } from '@iconify/vue';
    import { inject, computed } from 'vue';

    const { cart, removeFromCart, clearCart, updateQty, goToShop } = inject('cart')

    const totalItems = computed(() => {
      return cart.value.reduce((sum, item) => sum + item.qty, 0)
    })

    const totalHarga = computed(() => {
      return cart.value.reduce((sum, item) => sum + (item.harga * item.qty), 0)
    })

    const formatRp = (num) => {
      return new Intl.NumberFormat('id-ID').format(num)
    }

    const sendToWhatsApp = () => {
      let message = '*PESANAN KOKEDAMA*%0A%0A'
      
      cart.value.forEach((item, index) => {
        message += `${index + 1}. ${item.nama}%0A`
        message += `   Harga: Rp${formatRp(item.harga)}%0A`
        message += `   Jumlah: ${item.qty}%0A`
        message += `   Subtotal: Rp${formatRp(item.harga * item.qty)}%0A%0A`
      })
      
      message += `-----------------------------%0A`
      message += `*Total Harga: Rp${formatRp(totalHarga.value)}*%0A`
      message += `*Total Item: ${totalItems.value}*`

      const phoneNumber = '6289618324030' 
      const whatsappUrl = `https://wa.me/${phoneNumber}?text=${message}`
      
      window.open(whatsappUrl, '_blank')
    }

</script>

<template>
  <div class="px-4 pt-6 pb-35 flex flex-col gap-4">

    <!-- Title -->
    <h1 class="font-serif text-2xl text-green-950 font-bold">Keranjang</h1>

    <!-- Opsi -->
    <div class="flex justify-between items-center">
      <h5 class="text-sm text-gray-500">{{ totalItems }} Produk</h5>
      <button v-if="cart.length > 0" @click="clearCart" class="flex items-center gap-2 text-sm text-red-500 hover:text-red-600">
        Hapus Semua 
        <Icon icon="tabler:trash" width="18" height="18" />
      </button>
    </div>

    <!-- Empty State -->
    <div v-if="cart.length === 0" class="flex flex-col items-center justify-center py-12 gap-4">
      <Icon icon="mdi:cart-off" width="64" height="64" class="text-gray-300" />
      <p class="text-gray-500 text-center">Keranjang belum ada produk</p>
    </div>

    <!-- List Item -->
    <div v-else class="grid grid-cols-1 lg:grid-cols-3 gap-4">

      <!-- Item -->
      <div v-for="(item, index) in cart" :key="index" class="bg-white rounded-2xl p-3 flex gap-3 shadow-sm">

        <!-- Gambar -->
        <img :src="item.image" 
             class="w-24 h-24 object-cover rounded-xl">

        <!-- Detail -->
        <div class="flex flex-col justify-between w-full">

          <div>
            <h3 class="text-sm font-medium text-gray-800">
              {{ item.nama }}
            </h3>
            <h3 class="text-green-900 font-bold text-sm mt-1">
              Rp{{ formatRp(item.harga) }}
            </h3>
          </div>

          <!-- Quantity -->
          <div class="flex items-center justify-between mt-2">
            
            <div class="flex items-center border border-gray-300 rounded-lg overflow-hidden">
              <button @click="updateQty(index, item.qty - 1)" class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="lucide:minus" width="16" height="16" />
              </button>

              <input type="text" :value="item.qty" class="w-10 text-center text-sm outline-none" readonly>

              <button @click="updateQty(index, item.qty + 1)" class="px-2 py-1 hover:bg-gray-100">
                <Icon icon="ic:twotone-plus" width="16" height="16" />
              </button>
            </div>

            <!-- Optional delete per item -->
            <button @click="removeFromCart(index)" class="text-gray-400 hover:text-red-500">
              <Icon icon="mdi:trash-outline" width="18" height="18" />
            </button>

          </div>

        </div>
      </div>

    </div>

    <!-- Ringkasan -->
    <div v-if="cart.length > 0" class="bg-white rounded-2xl p-4 shadow-sm mt-4 flex flex-col gap-3">

      <h2 class="font-serif text-green-950 font-bold">
        Ringkasan Belanja
      </h2>

      <div class="flex justify-between text-sm text-gray-600 border-b pb-2">
        <span>Subtotal ({{ totalItems }} Produk)</span>
        <span>Rp{{ formatRp(totalHarga) }}</span>
      </div>

      <div class="flex justify-between font-bold text-green-900">
        <span>Total</span>
        <span>Rp{{ formatRp(totalHarga) }}</span>
      </div>

    </div>

    <!-- Action -->
    <div v-if="cart.length > 0" class="fixed bottom-0 left-0 w-full bg-white border-t p-4 grid grid-cols-1 lg:grid-cols-2 gap-2">

      <button @click="sendToWhatsApp" class="rounded-xl font-semibold bg-green-600 text-white py-3 hover:bg-green-700 transition flex items-center justify-center gap-2">
        <Icon icon="mdi:whatsapp" width="20" height="20" />
        Pesan via WhatsApp
      </button>

      <button @click="goToShop" class="border border-green-950 text-green-950 font-semibold rounded-xl py-3 hover:bg-green-50 transition">
        Lanjut Belanja
      </button>

    </div>

  </div>
</template>