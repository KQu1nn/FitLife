<template>
  <div
    class="fixed top-0 left-0 w-full z-50 flex flex-row justify-between border-b border-b-gray-200 px-5 md:px-17 py-3 items-center bg-gray-50">
    <p @click="scrollTo('top')" class="font-bold text-[25px] text-green-600 cursor-pointer">FitLife</p>

    <button @click="isOpen = !isOpen" class="md:hidden focus:outline-none">
      <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
        stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
        stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
      </svg>
    </button>

    <ul :class="[
      'flex flex-col md:flex-row gap-3 md:gap-16 text-[17px] text-gray-800 font-sans font-medium w-full md:w-auto transition-all duration-300 overflow-hidden',
      'absolute top-15 left-0 bg-white md:static md:bg-transparent',
      isOpen ? 'max-h-96 p-4' : 'max-h-0 md:max-h-full'     
    ]">
      <li @click="scrollTo('top')" class="cursor-pointer hover:text-green-500">Início</li>
      <li @click="scrollTo('produtos')" class="cursor-pointer hover:text-green-500">Produtos</li>
      <li @click="scrollTo('sobre')" class="cursor-pointer hover:text-green-500">Sobre</li>
      <li @click="scrollTo('endereco')" class="cursor-pointer hover:text-green-500">Endereço</li>
      <li><a
          href="https://api.whatsapp.com/send?phone=5599999999999&text=Ol%C3%A1%2C%20vim%20pelo%20seu%20site!">Contato</a>
      </li>
    </ul>
  </div>
</template>
<script setup>
const scrollTo = (id) => {
  const el = id === 'top' ? document.body : document.getElementById(id);
  if (el) {
    const yOffset = -60;
    const y = el.getBoundingClientRect().top + window.pageYOffset + yOffset;
    window.scrollTo({ top: y, behavior: 'smooth' });
  }
};
const isOpen = ref(false)
</script>