<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div class="min-vh-100 d-flex flex-column justify-content-center align-items-center  pt-sm-0 bg-light">
        <div class="">

            <Link href="/">
                <img src='http://127.0.0.1:8000/website/log-removebg-preview.png' class="w-100 m-auto d-inline-block ">
                <!-- <ApplicationLogo class="w-20 h-20 fill-current text-gray-500" /> -->
            </Link>
        </div>

        <div
            class="w-full mt-6 px-6 py-4  shadow-md overflow-hidden rounded-lg"
        >
            <slot />
        </div>
    </div>
</template>
