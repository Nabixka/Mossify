<script setup>
    import { Icon } from '@iconify/vue';
</script>

<template>
    <div class="pl-2 pr-2 flex flex-col gap-3">

        <!-- Title -->
        <h1 class="font-serif text-2xl text-green-950 font-bold">Keranjang</h1>

        <!-- Opsi -->
        <div class="flex justify-between">
            <h5 class="text-sm">3 Produk</h5>
            <h5 class="flex text-sm gap-3">Hapus Semua <Icon icon="tabler:trash" width="20" height="20" /></h5>
        </div>

        <!-- List -->
        <div class="grid grid-cols-1">

            <div class="p-1 rounded-lg bg-white/80 flex gap-2 items-center">

                <!-- Gambar -->
                <img src="/src/assets/kokedama.jpg" class="w-30 h-35 rounded-lg">

                <!-- Detail -->
                <div class="flex flex-col gap-3">
                    <h3 class="text-md">Kokedama Sirih Gading</h3>
                    <h3>Rp85.000</h3>

                    <div class="border border-gray-400 rounded-lg flex w-30">
                        <button class="border-r border-gray-200 py-1 px-2"><Icon icon="lucide:minus" width="24" height="24" /></button>
                        <input type="text" class="w-full text-center" placeholder="1">
                        <button class="border-l border-gray-200 px-2"><Icon icon="ic:twotone-plus" width="24" height="24" /></button>
                    </div>
                </div>
            </div>
            
            <div class="p-1 rounded-lg bg-white/80 flex gap-2 items-center">

                <!-- Gambar -->
                <img src="/src/assets/kokedama.jpg" class="w-30 h-35 rounded-lg">

                <!-- Detail -->
                <div class="flex flex-col gap-3">
                    <h3 class="text-md">Kokedama Sirih Gading</h3>
                    <h3>Rp85.000</h3>

                    <div class="border border-gray-400 rounded-lg flex w-30">
                        <button class="border-r border-gray-200 py-1 px-2"><Icon icon="lucide:minus" width="24" height="24" /></button>
                        <input type="text" class="w-full text-center" placeholder="1">
                        <button class="border-l border-gray-200 px-2"><Icon icon="ic:twotone-plus" width="24" height="24" /></button>
                    </div>
                </div>
            </div>

            <div class="p-1 rounded-lg bg-white/80 flex gap-2 items-center">

                <!-- Gambar -->
                <img src="/src/assets/kokedama.jpg" class="w-30 h-35 rounded-lg">

                <!-- Detail -->
                <div class="flex flex-col gap-3">
                    <h3 class="text-md">Kokedama Sirih Gading</h3>
                    <h3>Rp85.000</h3>

                    <div class="border border-gray-400 rounded-lg flex w-30">
                        <button class="border-r border-gray-200 py-1 px-2"><Icon icon="lucide:minus" width="24" height="24" /></button>
                        <input type="text" class="w-full text-center" placeholder="1">
                        <button class="border-l border-gray-200 px-2"><Icon icon="ic:twotone-plus" width="24" height="24" /></button>
                    </div>
                </div>
        
            </div>

            <!-- Ringkasan -->
            <div class="rounded-lg border border-gray-400 p-3 mt-5 mb-5">
                <h2 class="font-serif text-green-950">Ringkasan Belanja</h2>
                <h3 class="flex justify-between text-sm border-b pb-3 border-gray-300">Subtotal (3 Produk) <p>Rp265.000</p></h3>
                <div class="flex justify-between">
                    <h2>Total</h2>
                    <h2>Rp265.000</h2>
                </div>
            </div>

            <button class="mb-5 rounded-lg font-semibold bg-green-950 text-white py-2">Checkout</button>
            <button class="border border-green-950 text-green-950 font-semibold rounded-lg py-2">Lanjut Belanja</button>

        </div>

    </div>
</template>