<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
import SidebarLink from '@/Components/SidebarLink.vue';
</script>


<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <div class="flex h-screen w-full fixed">
            <!-- Sidebar -->
            <div class="bg-gray-800 text-white w-64 py-4">
                <!-- Enlace para el Dashboard -->
                <SidebarLink :href="route('dashboard')" :active="route().current('dashboard')">
                    Dashboard
                </SidebarLink>
                
                

                <!-- Otros enlaces del Sidebar -->
                <!-- <SidebarLink :href="route('example')" :active="route().current('example')">
                    Ejemplo
                </SidebarLink> -->
            </div>

            <!-- Contenido Principal -->
            <div class="flex-1 p-10">
                <div class="bg-white overflow-hidden shadow-sm sm:rounded-lg">
                    <div class="p-6 text-gray-900">You're logged in!</div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>

<style>
  body,
  html {
    margin: 0;
    padding: 0;
  }

  .flex {
    margin: 0;
  }
</style>