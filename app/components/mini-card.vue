<template>
    <div v-for="data in cardsData" class="w-[290px] h-[150px] shadow-2xl flex flex-col gap-1.5 items-center justify-center">
        <Icon :name="data.icon" size="32" class="text-green-600" />
        <h1 class="text-2xl font-bold">{{ data.title }}</h1>
        <p class="text-[17px] text-gray-500">{{ data.description }}</p>
    </div>
</template>
<script setup>
defineProps({
    cardsData: Array
})
</script>