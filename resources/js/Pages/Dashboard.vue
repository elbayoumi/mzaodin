<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-weight-bold h4 text-dark mb-4">Dashboard</h2>
        </template>

        <div class="py-12">
            <div class="container-fluid mx-auto px-4 px-sm-5">
                <div class="bg-white overflow-hidden shadow-sm rounded-lg">
                    <div class="p-6 text-dark">You're logged in!</div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
