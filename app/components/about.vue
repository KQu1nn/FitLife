<template>
    <div class="w-full min-h-screen flex flex-col md:flex-row px-8 gap-5 items-center justify-center bg-[#fafcfd]">
        <div class="w-full md:w-3/6 flex flex-col gap-8 justify-center items-center md:items-start">
            <h1 class="text-5xl text-black font-bold">Sobre a <span class="text-green-500">FitLife</span></h1>
            <p class="md:text-start text-center text-xl text-gray-400">
                A FitLife nasceu da paixão por fitness e da busca pela excelência. Oferecemos roupas esportivas de alta
                qualidade que combinam tecnologia avançada, design moderno e conforto incomparável.
                <br><br>
                Nossa missão é empoderar pessoas a alcançarem seus objetivos fitness com estilo e confiança,
                proporcionando
                peças que acompanham cada movimento do seu treino.
            </p>
            <ul class="flex flex-col gap-3">
                <li class="flex flex-row items-center gap-3 text-[17px] text-gray-800">
                    <Icon name="lucide:circle-check-big" size="23" class="text-green-600" />
                    Tecidos de alta performance
                </li>
                <li class="flex flex-row items-center gap-3 text-[17px] text-gray-800">
                    <Icon name="lucide:circle-check-big" size="23" class="text-green-600" />
                    Design moderno e funcional
                </li>
                <li class="flex flex-row items-center gap-3 text-[17px] text-gray-800">
                    <Icon name="lucide:circle-check-big" size="23" class="text-green-600" />
                    Qualidade premium garantida
                </li>
                <li class="flex flex-row items-center gap-3 text-[17px] text-gray-800">
                    <Icon name="lucide:circle-check-big" size="23" class="text-green-600" />
                    Sustentabilidade em primeiro lugar
                </li>
                <button class="w-50 my-5 bg-green-600/90 text-white px-2 py-2 rounded-sx font-medium cursor-pointer transform transition-transform duration-300 hover:scale-105"><a href="https://api.whatsapp.com/send?phone=5599999999999&text=Ol%C3%A1%2C%20vim%20pelo%20seu%20site!">Entre em Contato</a></button>
            </ul>
            
        </div>
        <div class="w-full md:w-3/6 flex flex-row flex-wrap gap-6 justify-center">
            <MiniCard :cardsData="cardsData" />
        </div>
    </div>
</template>
<script setup>
const cardsData = ref([
    {icon: "lucide:users", title: "10k+", description: "Clientes Satisfeitos"},
    {icon: "lucide:star", title: "4.9", description: "Avaliação Média"},
    {icon: "lucide:award", title: "5 Anos", description: "No Mercado"},
    {icon: "lucide:circle-check-big", title: "100%", description: "Garantia"},
])
</script>