<script setup>
    import { ref } from 'vue';
    import { Icon } from '@iconify/vue';

</script>

<template>
    <div class="flex flex-col gap-1 pl-5 pt-10 pr-5 pb-20">
        <h1 class="font-serif text-3xl text-green-950 font-bold">Shop</h1>
        <h3 class="font-semibold text-mist-500">Temukan kokedama favoritmu di sini</h3>

        <!-- Loop Kokedama -->
        <div class="grid grid-cols-2 gap-5 pt-14">
            <div class="bg-white border border-gray-200 rounded-xl overflow-hidden">
                <img src="/src/assets/kokedama.jpg" class="h-50 w-full">
                <div class="p-2 pb-5">
                    <h4 class="text-sm pb-2">Kokedama Sirih Gading</h4>
                    <h4>Rp85.000</h4>
                    <button class="mt-4 border border-green-800/80 rounded-lg w-full py-1 text-md">+ Keranjang</button>
                </div>
            </div>

            <div class="bg-white border border-gray-200 rounded-xl overflow-hidden">
                <img src="/src/assets/kokedama.jpg" class="h-50 w-full">
                <div class="p-2 pb-5">
                    <h4 class="text-sm pb-2">Kokedama Sirih Gading</h4>
                    <h4>Rp85.000</h4>
                    <button class="mt-4 border border-green-800/80 rounded-lg w-full py-1 text-md">+ Keranjang</button>
                </div>
            </div>

            <div class="bg-white border border-gray-200 rounded-xl overflow-hidden">
                <img src="/src/assets/kokedama.jpg" class="h-50 w-full">
                <div class="p-2 pb-5">
                    <h4 class="text-sm pb-2">Kokedama Sirih Gading</h4>
                    <h4>Rp85.000</h4>
                    <button class="mt-4 border border-green-800/80 rounded-lg w-full py-1 text-md">+ Keranjang</button>
                </div>
            </div>

            <div class="bg-white border border-gray-200 rounded-xl overflow-hidden">
                <img src="/src/assets/kokedama.jpg" class="h-50 w-full">
                <div class="p-2 pb-5">
                    <h4 class="text-sm pb-2">Kokedama Sirih Gading</h4>
                    <h4>Rp85.000</h4>
                    <button class="mt-4 border border-green-800/80 rounded-lg w-full py-1 text-md">+ Keranjang</button>
                </div>
            </div>
        </div>

        <!--  -->
        <div class="bg-gray-200 w-full rounded-lg p-3 mt-5 flex flex-col gap-3">
            <h3 class="font-serif flex items-center gap-3 font-bold text-green-800 text-xl">
                <Icon icon="meteor-icons:leaf" width="24" height="24" style="color: #233d1d"/>
                Custom Kokedama
            </h3>
            <h4 class="text-sm">Buat Kokedama sesuai keinginanmu!<br>Pilih tanaman, ukuran, dan gaya sendiri</h4>
            <button class="flex items-center text-sm gap-3 bg-white border border-gray-400 pl-3 font-semibold pr-2 py-2 rounded-lg w-1/2">Pesan Sekarang <Icon icon="maki:arrow" width="15" height="15" /></button>
        </div>
    </div>
</template>