<template>
<header class="border-b border-gray-200 dark:border-gray-700 dark:bg-gray-900 bg-white w-full">
    <div class="container mx-auto">
        <nav class="p-4 flex items-center justify-between">
            <div class="text-lg font-medium">
                <Link :href="route('listing.index')">Listings</Link>&nbsp;
            </div>
            <div class="text-xl font-bold text-indigo-600 dark:text-indigo-200">
                <Link :href="route('listing.index')">LaraZillow</Link>&nbsp;
            </div>
            <div class="text-xl text-indigo-600 dark:text-indigo-200">
                <Link :href="route('listing.create')" class="btn-primary">+ New Listing</Link>
            </div>
        </nav>
    </div>
</header>
<main class="container mx-auto p-4">
    <div v-if="flashSuccess" class="mb-4 px-2 border rounded-md shadow-sm border-green-200 bg-green-50">
        {{flashSuccess}}
    </div>
    <slot />
</main>

</template>

<script setup>
import {Link, usePage} from '@inertiajs/vue3';
import {computed} from "vue";

const page = usePage()
const flashSuccess = computed(
    () => page.props.flash.success
)
</script>
