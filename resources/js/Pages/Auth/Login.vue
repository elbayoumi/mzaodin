<script setup>
import Checkbox from '@/Components/Checkbox.vue';
import GuestLayout from '@/Layouts/GuestLayout.vue';
import InputError from '@/Components/InputError.vue';
import InputLabel from '@/Components/InputLabel.vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import TextInput from '@/Components/TextInput.vue';
import { Head, Link, useForm } from '@inertiajs/vue3';

defineProps({
    canResetPassword: {
        type: Boolean,
    },
    status: {
        type: String,
    },
});

const form = useForm({
    email: '',
    password: '',
    remember: false,
});

const submit = () => {
    form.post(route('login'), {
        onFinish: () => form.reset('password'),
    });
};
</script>

<template>
    <GuestLayout>

        <Head title="Log in" />

        <div v-if="status" class="mb-4 font-medium small text-success">
            {{ status }}
        </div>

        <form @submit.prevent="submit">
            <div>
                <div class="form-group">

                    <InputLabel for="email" value="Email" />

                    <TextInput id="email" type="email" class="form-control" v-model="form.email" required autofocus
                        autocomplete="username" />

                    <InputError class="mt-2" :message="form.errors.email" />
                </div>
            </div>

            <div class="mt-4">
                <div class="form-group">

                    <InputLabel for="password" value="Password" />

                    <TextInput id="password" type="password" class="form-control" v-model="form.password" required
                        autocomplete="current-password" />

                    <InputError class="mt-2" :message="form.errors.password" />
                </div>
            </div>

            <div class="block mt-4">
                <label class="flex items-center">
                    <Checkbox name="remember" v-model:checked="form.remember" />
                    <span class="ms-2 small text-secondary">Remember me</span>
                </label>
            </div>

            <div class="d-flex align-items-center justify-content-end mt-4">
                <Link v-if="canResetPassword" :href="route('password.request')"
                    class="text-sm text-gray-600 text-decoration-none d-inline-block rounded-md">
                Forgot your password?
                </Link>

                <PrimaryButton class="btn btn-main" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Log in
                </PrimaryButton>
            </div>
        </form>
    </GuestLayout>
</template>
