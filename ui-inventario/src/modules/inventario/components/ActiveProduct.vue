<template>
  <div class="text-center text-sm space-y-2">
    <p class="font-bold text-lg">Paleta</p>
    <p>Cantidad</p>
    <div
      class="size-20 text-xl font-black border border-slate-200 p-2 mx-auto leading-0 rounded-full grid place-items-center"
    >
      20
    </div>
    <div class="flex gap-3 justify-center">
      <button><PlusCircleIcon /></button>
      <button><CircleMinusIcon /></button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { CircleMinusIcon, PlusCircleIcon } from 'lucide-vue-next'
</script>
