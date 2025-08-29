<template>
    <div class="w-full flex flex-col gap-5 items-center justify-center px-10 py-17">
        <h1 class="text-3xl font-bold">Siga no <span class="text-green-500">Instagram</span></h1>
        <p class="text-xl text-gray-500">Acompanhe nosso dia a dia, novidades e inspirações fitness</p>
        <button class="bg-green-500 text-white px-6 py-2.5 cursor-pointer rounded-sx flex flex-row gap-1.5 items-center">
            <Icon name="lucide:instagram" size="17" class="text-white" />
            @fitlife
        </button>
    </div>
    <div class="w-full flex flex-row flex-wrap justify-center md:justify-between px-10 items-center py-10">
        <InstagramCard />
        <InstagramCard />
        <InstagramCard />
        <InstagramCard />
        <InstagramCard />
        <InstagramCard />
    </div>
</template>