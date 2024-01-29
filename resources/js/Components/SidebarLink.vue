<script setup>
import { defineProps, computed } from 'vue';
import { Link } from '@inertiajs/vue3';

const props = defineProps({
  href: {
    type: String,
    required: true,
  },
  active: {
    type: Boolean,
  },
});

const classes = computed(() =>
  props.active
    ? 'block pl-3 pr-4 py-2 bg-gray-900 text-white font-medium transition duration-300 ease-in-out'
    : 'block pl-3 pr-4 py-2 text-gray-700 hover:bg-indigo-600 hover:text-white transition duration-300 ease-in-out'
);
</script>

<template>
  <Link :href="href" :class="classes">
    <slot />
  </Link>
  
</template>

