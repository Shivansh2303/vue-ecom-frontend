<!-- route is "/products/:id" -->
<!-- [] in file name shows that path of the route is changable -->
<template>
    <div>

        <Head>
            <Title>Nust Dojo | {{ product.title }}</Title>
            <!-- <Meta name:'description':content="product.description" /> -->
        </Head>
        <ProductDetails :product="product" />
    </div>
</template>

<script setup>
import { useRoute } from 'vue-router'

const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id

// fetch the product 
const { data: product } = await useFetch(uri, { key: id })
if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: 'Product not found', fatal: true })
}
definePageMeta({
    layout: 'products'
})
</script>

<style  scoped></style>