<script setup>
import { computed } from "vue";
const props = defineProps({
  alerta: {
    type: Object,
    required: true,
  },
});
const isError = computed(() => props.alerta.tipo === "error");
</script>
<template>
  <div
    :class="isError ? 'bg-red-500 ' : 'bg-green-500 '"
    class="text-white text-center uppercase font-bold mb-4 rounded-md py-3 px-5"
  >
    {{ alerta.mensaje }}
  </div>
</template>
