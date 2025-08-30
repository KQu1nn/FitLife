<template>
    <div class="fixed top-0 left-0 w-full z-50 flex flex-row justify-between border-b border-b-gray-200 px-17 py-3 items-center bg-gray-50">
        <p @click="scrollTo('top')" class="font-bold text-[25px] text-green-600 cursor-pointer">FitLife</p>
        <ul class="flex flex-row gap-16 text-[17px] text-gray-800 font-sans font-medium">
            <li @click="scrollTo('top')" class="cursor-pointer hover:text-green-500">Início</li>
            <li @click="scrollTo('produtos')" class="cursor-pointer hover:text-green-500">Produtos</li>
            <li @click="scrollTo('sobre')" class="cursor-pointer hover:text-green-500">Sobre</li>
            <li @click="scrollTo('endereco')" class="cursor-pointer hover:text-green-500">Endereço</li>
            <li><a href="https://api.whatsapp.com/send?phone=5599999999999&text=Ol%C3%A1%2C%20vim%20pelo%20seu%20site!">Contato</a></li>
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
</script>