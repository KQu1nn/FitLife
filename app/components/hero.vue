<template>
    <div class="w-full py-35 text-white flex flex-col justify-center items-center gap-7">
        <h1 class="text-7xl font-bold">FitLife</h1>
        <p class="w-3/6 text-2xl text-center">Eleve seu treino ao próximo nível com roupas fitness que combinam
            <span class="text-green-600 font-bold">performance e estilo</span>
        </p>
        <div class="flex flex-row gap-4 font-bold items-center">
            <button @click="scrollTo('produtos')"
                class="cursor-pointer text-lg text-white bg-green-600 px-9 py-2 rounded-xs transform transition-transform duration-300 hover:scale-105">Ver
                Produtos</button>
            <button @click="scrollTo('sobre')" class="cursor-pointer text-lg text-black bg-white px-9 py-2 rounded-xs ">Sobre nós</button>
        </div>
    </div>
    <div class="w-full flex justify-center">
        <Icon @click="scrollTo('produtos')" name="lucide:arrow-down" size="32" class="text-white animate-bounce" />
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