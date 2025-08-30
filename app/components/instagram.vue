<template>
    <div class="w-full flex flex-col gap-5 items-center justify-center  px-10 pt-30 pb-10 md:pb-0 md:py-10 bg-[#fafcfd]">
        <h1 class="text-3xl font-bold">Siga no <span class="text-green-500">Instagram</span></h1>
        <p class="text-xl text-gray-500">Acompanhe nosso dia a dia, novidades e inspirações fitness</p>
        <a href="https://instagram.com/#">
            <button
                class="bg-green-500 font-bold text-lg text-white px-6 py-2.5 cursor-pointer rounded-sx flex flex-row gap-1.5 items-center">
                <Icon name="lucide:instagram" size="20" class="text-white" />
                @fitlife
            </button>
        </a>
    </div>
    <div class="w-full flex flex-row flex-wrap justify-center md:justify-between gap-1 md:gap-0 px-10 md:py-20 items-center bg-[#fafcfd]">
        <InstagramCard v-for="data in instagramCart" :data="data" />
    </div>
</template>
<script setup>
import image01 from '@/assets/images/image01.jpg'
import image02 from '@/assets/images/image02.jpg'
import image03 from '@/assets/images/image03.jpg'
import image04 from '@/assets/images/image04.jpg'
import image05 from '@/assets/images/image05.jpg'

const instagramCart = ref([
    { image: image01, likes: 100, url: 'https://instagram.com/#' },
    { image: image02, likes: 200, url: 'https://instagram.com/#1' },
    { image: image03, likes: 140, url: 'https://instagram.com/#2' },
    { image: image04, likes: 170, url: 'https://instagram.com/#3' },
    { image: image05, likes: 50, url: 'https://instagram.com/#4' },
    { image: image04, likes: 346, url: 'https://instagram.com/#5' },
])

</script>