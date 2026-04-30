<script setup>
    import { Icon } from '@iconify/vue';
</script>

<template>
    <div class="mb-20">

        <!-- Title -->
        <h1 class="mt-5 ml-3 font-serif text-2xl text-green-950 font-bold">About Kokedama</h1>
        <h5 class="mt-5 ml-3 mr-2">Seni tanaman yang membawa keindahan alam lebih dekat denganmu</h5>

        <!-- Pengertian -->
        <div class="bg-white mt-5 p-3">
            <div class="flex items-center gap-8">
                <div class="flex flex-col gap-3">
                    <h3 class="font-serif font-semibold text-lg text-green-950">Apa itu Kokedama?</h3>
                    <h5 class="text-xs">kokedama adalah seni menanam asal jepang yang menggunakan bola tanah yang dibungkus dengan lumut. Tanaman ditanam tanpa pot, sehingga memberikan kesan alam, minimalis, dan menenangkan</h5>
                </div>
                <img src="/src/assets/kokedama.jpg" class="w-35 h-40 rounded-lg">
            </div>

            <div class="grid grid-cols-2 gap-3 pt-5">

                <div class="flex justify-center gap-1 flex-col items-center">
                    <Icon icon="meteor-icons:leaf" width="24" height="24" style="color: #233d1d"/>
                    <h3 class="text-green-950 font-semibold">Alami</h3>
                    <h4 class="text-center text-sm text-mist-500">Menggunakan bahan alami dan ramah lingkungan</h4>
                </div>

                <div class="flex justify-center gap-1 flex-col items-center">
                    <Icon icon="charm:plant-pot" width="24" height="24" style="color: #233d1d"/>
                    <h3 class="text-green-950 font-semibold">Estetis</h3>
                    <h4 class="text-center text-sm text-mist-500">Mempercantik ruangan dengan sentuhan hijau alami</h4>
                </div>

                <div class="flex justify-center gap-1 flex-col items-center">
                    <Icon icon="boxicons:water-spray" width="24" height="24" style="color: #233d1d"/>
                    <h3 class="text-green-950 font-semibold">Estetis</h3>
                    <h4 class="text-center text-sm text-mist-500">Mempercantik ruangan dengan sentuhan hijau alami</h4>
                </div>

                <div class="flex justify-center gap-1 flex-col items-center">
                    <Icon icon="mdi:present" width="24" height="24" style="color: #233d1d"/>
                    <h3 class="text-green-950 font-semibold">Hadiah Spesial</h3>
                    <h4 class="text-center text-sm text-mist-500">Pilih hadiah unik untuk orang tersayang</h4>
                </div>

            </div>
        </div>

        <div class="pl-3 pt-5">
            <h3 class="font-serif text-green-950 font-semibold text-lg">Manfaat Kokedama</h3>
            <div>
                <h3 class="flex items-center gap-2 text-sm"><Icon icon="mingcute:check-fill" width="16" height="16" style="color: #233d1d"/>Membantu menyegarkan udara</h3>
                <h3 class="flex items-center gap-2 text-sm"><Icon icon="mingcute:check-fill" width="16" height="16" style="color: #233d1d"/>Meningkatkan suasana hati dan mengurangi stres</h3>
                <h3 class="flex items-center gap-2 text-sm"><Icon icon="mingcute:check-fill" width="16" height="16" style="color: #233d1d"/>Menambah keindahan dekorasi ruangan</h3>
                <h3 class="flex items-center gap-2 text-sm"><Icon icon="mingcute:check-fill" width="16" height="16" style="color: #233d1d"/>Cocok untuk berbagai jenis tanaman indoor</h3>
            </div>
        </div>

    </div>
</template>