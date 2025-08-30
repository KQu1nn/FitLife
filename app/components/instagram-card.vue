<template>
    <div class="relative md:w-50 md:h-50 overflow-hidden cursor-pointer group">
        <a :href="data.url">
            <img :src="data.image"
                class="w-full h-full object-cover transition-transform duration-300 ease-in-out group-hover:scale-105" />

            <div class="absolute inset-0 bg-black/0 transition duration-300 group-hover:bg-black/40"></div>

            <div class="absolute bottom-2 left-2 text-white w-full px-2 flex flex-row gap-1 items-center z-10">
                <Icon name="lucide:instagram" size="17" class="text-white" />
                {{ data.likes }} likes
            </div>
        </a>

    </div>
</template>
<script setup>

defineProps({
    data: Object
})
</script>
