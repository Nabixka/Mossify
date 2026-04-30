<script setup>
import Home from './components/Home.vue'
import Shop from './components/Shop.vue'
import Cart from './components/Cart.vue'
import About from './components/About.vue'
import { Icon } from '@iconify/vue'
import { ref } from 'vue'

const isShow = ref(false)
const handleSection = ref('home')

const navItems = [
  { id: 'home', label: 'Home' },
  { id: 'shop', label: 'Shop' },
  { id: 'about', label: 'About' },
]
</script>

<template>
  <div class="min-h-screen bg-slate-50 text-slate-900">
    <header class="sticky top-0 z-50 border-b border-slate-200/80 bg-white/90 backdrop-blur-xl shadow-sm">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-4 py-4 sm:px-6">
        <div class="flex items-center gap-3">
          <button @click="isShow = !isShow" class="rounded-full border border-slate-200 bg-slate-50/80 p-2 text-slate-600 transition hover:bg-slate-100">
            <Icon icon="ci:hamburger-lg" width="26" height="26" />
          </button>
          <div>
            <p class="text-xs uppercase tracking-[0.3em] text-emerald-700">Mossify</p>
            <h1 class="text-xl font-semibold text-slate-900">Kokedama Shop</h1>
          </div>
        </div>

        <div class="hidden items-center gap-3 md:flex">
          <button
            v-for="item in navItems"
            :key="item.id"
            @click="handleSection = item.id"
            :class="['rounded-full px-4 py-2 text-sm font-medium transition', handleSection === item.id ? 'bg-emerald-700 text-white' : 'text-slate-600 hover:bg-slate-100']">
            {{ item.label }}
          </button>
        </div>

        <button @click="handleSection = 'cart'" class="inline-flex items-center gap-2 rounded-full bg-emerald-700 px-4 py-2 text-sm font-semibold text-white shadow-sm transition hover:bg-emerald-800">
          <Icon icon="mdi:cart" width="20" height="20" />
          Keranjang
        </button>
      </div>

      <div v-if="isShow" class="border-t border-slate-200 bg-slate-50/95 px-4 py-4 md:hidden">
        <div class="flex flex-col gap-3">
          <button
            v-for="item in navItems"
            :key="item.id"
            @click="handleSection = item.id; isShow = false"
            class="rounded-2xl border border-slate-200 bg-white px-4 py-3 text-left text-slate-700 transition hover:bg-slate-100">
            {{ item.label }}
          </button>
        </div>
      </div>
    </header>

    <main class="mx-auto max-w-6xl px-4 py-8 sm:px-6">
      <section v-if="handleSection === 'home'">
        <Home />
      </section>

      <section v-else-if="handleSection === 'shop'">
        <Shop />
      </section>

      <section v-else-if="handleSection === 'about'">
        <About />
      </section>

      <section v-else-if="handleSection === 'cart'">
        <Cart />
      </section>
    </main>
  </div>
</template>
