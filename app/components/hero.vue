<template>
    <div class="w-full min-h-screen text-white flex flex-col justify-center items-center gap-10 md:gap-7" :style="{ minHeight: 'calc(100vh - 100px)' }">
        <h1 class="text-7xl font-bold">FitLife</h1>
        <p class=" md:w-3/6 text-xl px-5 md:px-0 md:text-2xl text-center">Eleve seu treino ao próximo nível com roupas fitness que combinam
            <span class="text-green-600 font-bold">performance e estilo</span>
        </p>
        <div class="flex flex-row gap-4 font-bold items-center">
            <button @click="scrollTo('produtos')"
                class="cursor-pointer text-lg text-white bg-green-600 px-5 md:px-9 py-2 rounded-xs transform transition-transform duration-300 hover:scale-105">Ver
                Produtos</button>
            <button @click="scrollTo('sobre')" class="cursor-pointer text-lg text-black bg-white px-5 md:px-9 py-2 rounded-xs ">Sobre nós</button>
        </div>
    </div>
    <div class="w-full flex justify-center">
        <Icon @click="scrollTo('produtos')" name="lucide:arrow-down" size="32" class="text-white animate-bounce py-5 md:py-8" />
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