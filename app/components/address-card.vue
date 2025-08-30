<template>
    <div v-for="(data, index) in cardsData" :key="index" class="w-full flex flex-row gap-5 p-6 shadow-xs border border-gray-200/90 rounded-xs">
        <div class="bg-green-200/40 w-12 h-12 flex items-center justify-center">
            <Icon :name="data.icon" size="25" class="text-green-600" />
        </div>
        <div class="flex flex-col gap-4">
            <h3 class="text-[22px] font-bold">{{ data.title }}</h3>
            <p v-html="data.description" class=" text-lg text-gray-700/80">
            </p>
        </div>
    </div>
</template>
<script setup>
defineProps({
    cardsData: Array
})
</script>