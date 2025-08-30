<template>
    <div class="w-full min-h-screen bg-[url('@/assets/images/hero.jpg')] bg-cover bg-center relative">
        <div class="absolute inset-0 bg-gradient-to-br from-gray-900/90 via-gray-900/80 to-green-700/90"></div>

        <div class="relative z-10">
            <Nav />
            <Hero />
        </div>
    </div>
    <div>
        <div class="w-full flex flex-col gap-7 items-center justify-center px-10 py-17">
            <h1 class="text-5xl font-bold">Nossos <span class="text-green-600">Produtos</span></h1>
            <p class="w-7/12 text-center text-xl text-gray-500 ">Descubra nossa coleção exclusiva de roupas fitness que combinam tecnologia, conforto e estilo para elevar
                seus treinos</p>
        </div>
        <div class="flex flex-row flex-wrap gap-8 justify-center pb-20">
            <ProductCard :products="products" />
        </div>
    </div>
    <About />
    <Instagram />
    <Address />
</template>
<script setup>
import product1 from '@/assets/images/product1.jpg'
import product2 from '@/assets/images/product2.jpg'
import product3 from '@/assets/images/product3.jpg'
import product4 from '@/assets/images/product4.jpg'
import product5 from '@/assets/images/product5.jpg'
import product6 from '@/assets/images/product6.jpg'

const products = ref([
    {id: 1, name: 'Legging High Performance', description: 'Legging de alta performance com tecido que não marca e máxima elasticidade', price: '89,90', url: product1},
    {id: 2, name: 'Top Esportivo Pro', description: 'Top com suporte médio ideal para treinos intensos', price: '49,90', url: product2},
    {id: 3, name: 'Shorts Masculino Dry Fit', description: 'Shorts com tecnologia dry fit para máxima ventilação', price: '59,90', url: product3},
    {id: 4, name: 'Regata Tank Premium', description: 'Regata masculina em tecido premium para treinos', price: '39,90', url: product4},
    {id: 5, name: 'Conjunto Feminino Comfort', description: 'Conjunto completo com legging e top para máximo conforto', price: '119,90', url: product5},
    {id: 6, name: 'Moletom Fitness Unissex', description: 'Moletom leve e confortável para aquecimento', price: '89,90', url: product6},
])
</script>