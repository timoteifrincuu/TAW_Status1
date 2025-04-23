<template>
    <div class="flex flex-col min-h-screen">
      <Header />
      <main class="flex items-center justify-center min-h-screen bg-orange-200">
        <div class="flex flex-col items-center space-y-6 p-6 bg-white shadow-lg rounded-lg">
          <h1 class="text-2xl font-bold text-orange-950">Programează-te</h1>
  
          <div class="flex flex-col items-start space-y-2">
            <label for="date" class="text-sm font-medium text-gray-700">Selectează o dată:</label>
            <input id="date" type="date"
              class="border rounded-lg px-4 py-2 w-full focus:ring focus:ring-orange-300" />
          </div>
  
          <div class="flex flex-col items-start space-y-2">
            <label for="time" class="text-sm font-medium text-gray-700">Selectează o oră:</label>
            <input id="time" type="time"
              class="border rounded-lg px-4 py-2 w-full focus:ring focus:ring-orange-300" />
          </div>
  
          <button @click="goToAccount"
            class="rounded-lg bg-orange-950 hover:bg-orange-800 text-orange-200 py-2 px-4 w-full font-semibold">
            Confirmă Programarea
          </button>
        </div>
      </main>
      <Footer />
    </div>
  </template>
  
  <script setup>
  import Footer from './Footer.vue';
  import Header from './Header.vue';
  import { useRouter } from 'vue-router';
  const router = useRouter(); 
  const goToAccount = () => {
    router.push('/account');
  };
  </script>
  