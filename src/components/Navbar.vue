<script setup></script>

<template>
    <nav class="z-50 bg-white">
      <div class="flex justify-between p-3">
        <button @click="isShow = !isShow">
          <Icon icon="ci:hamburger-lg" width="27" height="27" />
        </button>
        <div>
          <h3>Mossify</h3>
        </div>
        <Icon icon="mdi:cart" width="24" height="24" />
      </div>

      <div v-if="isShow" class="bg-gray-200 pl-5 pr-5 pt-7 text-center flex flex-col gap-3 pb-5">
        <h3 class="border border-green-950 py-1 rounded-lg">Home</h3>
        <h3 class="border border-green-950 py-1 rounded-lg">Shop</h3>
        <h3 class="border border-green-950 py-1 rounded-lg">About</h3>
      </div>
    </nav>
</template>