<script setup>
import {Link} from "@inertiajs/vue3";
import NavLink from "@/Components/BaseInput/front/NavLink.vue";
import ApplicationLogo from "@/Components/BaseInput/ApplicationLogo.vue";
</script>

<template>
  <nav class="bg-gray-700 fixed w-full z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="flex w-full justify-between">
          <!-- Logo -->
          <div class="shrink-0 flex items-center">
            <Link :href="route('home')">
              <ApplicationLogo
                  class="block h-16 w-auto fill-current text-white"
              />
            </Link>
          </div>

          <div class="hidden sm:-my-px sm:ms-10 sm:flex sm:gap-4">
            <NavLink :href="route('login')" :active="route().current('login')">
              Connexion
            </NavLink>
            <NavLink :href="route('register')" :active="route().current('register')">
              Inscription
            </NavLink>
          </div>
        </div>
      </div>
    </div>
  </nav>
  <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100">
    <slot name="main"/>
  </div>
</template>