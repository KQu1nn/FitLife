<template>
    <div class="w-full min-h-screen py-15 px-10 pb-20 items-center">
        <div class="w-full flex flex-col gap-5 items-center justify-center py-10">
            <h1 class="text-5xl font-bold">Nossa <span class="text-green-500">Localização</span></h1>
            <p class="w-5/12 text-center text-xl text-gray-500">Venha nos visitar na nossa loja física! Estamos no
                coração de São Paulo</p>
        </div>
        <div class="w-full flex flex-row gap-10 items-center">
            <div class="w-[610px] flex flex-col gap-6">
                <ClientOnly>
                    <AddressCard :cardsData="cardsData" />
                </ClientOnly>
            </div>
            <div class="w-[610px] h-[380px]">
                <div class="w-full h-[380px] rounded-sm shadow-md">
                    <iframe
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3656.9305831982176!2d-46.63961948450478!3d-23.5489439846904!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce59c8e962d6f1%3A0x2f8c99e81f5d0d7!2sFit%20Academy!5e0!3m2!1spt-BR!2sbr!4v1693305600000!5m2!1spt-BR!2sbr"
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>

                </div>
                <div class="w-full flex flex-col items-center text-center text-md py-5">
                    <p class="font-bold text-gray-600">📍 A 5 minutos da estação de metrô Sé</p>
                    <p class="text-gray-600">🚗 Estacionamento conveniado na esquina</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
const cardsData = [
    {
        icon: 'lucide:map-pin', title: 'FitLife Store',
        description: `<p>Rua das Academias, 123</p> <p>Centro - São Paulo, SP</p> <p>CEP: 01234-567</p>`
    },
    {
        icon: 'lucide:clock', title: 'Horários',
        description: `<p><span class="font-bold">Segunda à Sexta:</span> 8h às 18h </p> <p><span class="font-bold">Sábado:</span> 8h às 12h </p> <p><span class="font-bold">Domingo:</span> Fechado </p>`
    },
    {
        icon: 'lucide:phone', title: 'Contato',
        description: `<p><span class="font-bold">WhatsApp:</span> (11) 99999-9999</p> <p><span class="font-bold">Telefone:</span> (11) 3333-3333</p>`
    },
]
</script>