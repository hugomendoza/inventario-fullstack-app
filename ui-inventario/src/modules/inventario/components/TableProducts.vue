<template>
  <div class="relative overflow-x-auto shadow sm:rounded-lg">
    <table class="w-full text-sm text-gray-500 whitespace-nowrap">
      <thead class="text-xs text-gray-700 uppercase bg-gray-50">
        <tr>
          <th scope="col" class="px-6 py-3">Producto</th>
          <th scope="col" class="px-6 py-3">Descripcion</th>
          <th scope="col" class="px-6 py-3">Cantidad</th>
          <th scope="col" class="px-6 py-3">Precio</th>
          <th scope="col" class="px-6 py-3">Total</th>
          <th scope="col" class="px-6 py-3">
            <span class="sr-only">Acciones</span>
          </th>
        </tr>
      </thead>
      <tbody>
        <tr class="bg-white border-b border-gray-200 hover:bg-gray-50">
          <th scope="row" class="px-6 py-3 font-medium text-gray-900">
            Paleta
          </th>
          <td class="px-6 py-3 truncate">Lorem ipsum dolor sit amet</td>
          <td class="px-6 py-3">300</td>
          <td class="px-6 py-3">$2999</td>
          <td class="px-6 py-3">$9990</td>
          <td class="px-6 py-3 text-right">
            <a href="#" class=""><Trash2 :size="20" /> </a>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script lang="ts" setup>
import { Trash2 } from 'lucide-vue-next'
</script>
