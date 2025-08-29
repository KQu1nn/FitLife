<template>
    <div v-for="product in products" :key="product.id" class="w-[405px] flex flex-col rounded-xs cursor-pointer shadow-xs hover:shadow-xl transition duration-200 group">
        <div class=" h-64 w-[405px] overflow-hidden">
            <img class="w-full h-full rounded-xs object-cover transition-transform duration-300 ease-in-out group-hover:scale-110" 
                :src="product.url" alt="">
        </div>
        <div class="p-5 flex flex-col gap-2">
            <h2 class="text-[21px] font-bold">{{ product.name }}</h2>
            <p class="text-[18px] text-gray-500">{{ product.description }}</p>
            <div class="w-full flex flex-row justify-between">
                <p class="text-2xl text-green-600 font-bold">R$ {{ product.price }}</p>
                <button class="bg-green-600/90 text-white px-3 py-2 rounded-sx">Comprar</button>
            </div>
        </div>
    </div>
</template>
<script setup>
defineProps({
    products: Array
})
</script>