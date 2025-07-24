<template>
  <div>
    <!-- Header / Navbar Section -->
    <nav class="bg-slate-950 w-full">
      <div class="flex justify-between items-center px-4 py-2 md:px-6">
        <!-- Hamburger Icon (Mobile Only) -->
        <button @click="isOpen = !isOpen" class="text-white text-3xl md:hidden">
          <span v-if="!isOpen">☰</span>
          <span v-else>✖</span>
        </button>

        <!-- Nav Links (Desktop) -->
        <ul class="hidden md:flex space-x-4 px-2">
          <a href="">
            <li class="text-white py-3 px-4 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Individuals</li>
          </a>
          <a href="">
            <li class="text-white py-3 px-4 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Businesses</li>
          </a>
          <a href="">
            <li class="text-white py-3 px-4 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Universities</li>
          </a>
          <a href="">
            <li class="text-white py-3 px-4 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Governments</li>
          </a>
        </ul>
      </div>

      <!-- Mobile Menu Items -->
      <ul v-if="isOpen" class="md:hidden flex flex-col px-2 space-y-2 pb-3 bg-slate-950">
        <a href="">
          <li class="text-white py-2 px-3 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Individuals</li>
        </a>
        <a href="">
          <li class="text-white py-2 px-3 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Businesses</li>
        </a>
        <a href="">
          <li class="text-white py-2 px-3 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Universities</li>
        </a>
        <a href="">
          <li class="text-white py-2 px-3 hover:bg-white hover:text-black cursor-pointer transition duration-300">For Governments</li>
        </a>
      </ul>
    </nav>

    <!-- Logo + Explore + Search Section -->
    <div id="searchbar" class="flex flex-col md:flex-row justify-between items-center px-4 py-4 gap-4 md:gap-6">
      <!-- Logo + Explore + Search -->
      <div class="flex flex-col md:flex-row gap-4 items-center w-full">
        <!-- Logo -->
        <h1 class="text-blue-700 text-3xl font-bold">Coursera</h1>

        <!-- Explore -->
        <a href="" class="text-slate-800 hover:bg-yellow-50 px-3 py-2 rounded-md whitespace-nowrap">Explore</a>

        <!-- Search Input -->
        <input
          type="search"
          placeholder="What do you want to learn"
          class="px-4 py-3 border border-black opacity-40 outline-none rounded-3xl w-full md:w-[400px] text-sm"
        />
      </div>

      <!-- Login + Join -->
      <div class="flex gap-4 items-center">
        <a href="" class="text-blue-600 hover:underline">Login</a>
        <a href="">
          <button class="border px-2 w-[120px] py-2 rounded-md border-blue-800 text-blue-600 hover:bg-blue-50 text-[15px] transition">
            Join for Free
          </button>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const isOpen = ref(false)
</script>
