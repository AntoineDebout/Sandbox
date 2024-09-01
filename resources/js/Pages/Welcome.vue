<script setup>
import { Head } from '@inertiajs/vue3';
import FrontLayout from "@/Layouts/FrontLayout.vue";
</script>

<template>
  <Head title="Homepage" />

  <FrontLayout>
    <template #main>
        <h1 class="text-black">Hello</h1>
    </template>
  </FrontLayout>
</template>
