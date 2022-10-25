<script setup lang="ts">
import { ref } from "vue";
import Sidebar from "./Sidebar.vue";
const show = ref(false);
</script>

<template>
  <button
    class="bg-violet-500 py-2 px-4 text-white rounded-md hover:bg-violet-600"
    v-on:click="show = !show"
  >
    Open Sidebar
  </button>
  <Sidebar :show="show" v-on:close="show = false">
    <h3
      class="text-center bg-gradient-to-b from-sky-400 to-sky-600 text-white py-2"
    >
      This is a sidebar
    </h3>
  </Sidebar>
</template>
