<script setup lang="ts">
defineProps<{ show: boolean }>();
defineEmits(["close"]);
</script>
<template>
  <div
    v-if="show"
    class="h-screen fixed top-0 right-0 w-full bg-black/25 backdrop-blur"
  ></div>
  <div
    class="fixed bg-slate-200 w-48 h-screen top-0 transition-all duration-500"
    :class="show ? 'right-0' : '-right-full'"
  >
    <div
      v-on:click="$emit('close')"
      class="absolute cursor-pointer m-1 hover:text-red-500 transition"
    >
      x
    </div>
    <slot></slot>
  </div>
</template>
