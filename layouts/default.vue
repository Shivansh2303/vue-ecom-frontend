<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between ">
                <NuxtLink to="/" class="font-bold">Nuxt Dojo</NuxtLink>
                <ul class="flex gap-4">
                    <!-- Anchor tag alternative 
                if we user anchor tag for pages route this will send a fresh request to servre  4
                instead we want to swap out the component of waht pages we are headed to so we use nuctlink-->
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/products" class="bg-[#12b488] text-white px-3 py-2 rounded-md text-sm text-white">Products</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
        <!-- Output the page content -->
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>      

<style scoped>
.router-link-exact-active {
    color: #12b488;
}
</style>