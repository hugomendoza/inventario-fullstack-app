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
        <tr
          v-for="product in products"
          :key="product.id"
          class="bg-white border-b border-gray-200 hover:bg-gray-50"
        >
          <th scope="row" class="px-6 py-3 font-medium text-gray-900">
            {{ product.name }}
          </th>
          <td class="px-6 py-3 truncate">
            {{
              product.description.length > 25
                ? product.description.slice(0, 25) + '...'
                : product.description
            }}
          </td>
          <td class="px-6 py-3">{{ product.quantity }}</td>
          <td class="px-6 py-3">{{ product.price }}</td>
          <td class="px-6 py-3">{{ totalPrice }}</td>
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
import type { Product } from '../interfaces/product.interface'
import { computed } from 'vue'

interface Props {
  products: Product[]
}

const { products } = defineProps<Props>()

const totalPrice = computed(() => {
  return products.reduce((total, product) => {
    return total + product.price * product.quantity
  }, 0)
})
</script>
