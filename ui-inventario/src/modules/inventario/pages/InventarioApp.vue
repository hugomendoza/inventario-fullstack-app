<template>
  <!-- formulario -->
  <main class="bg-slate-100 min-h-dvh p-4">
    <div class="max-w-6xl mx-auto bg-white rounded-3xl p-6 shadow-md">
      <section class="border border-slate-200 rounded-xl p-6 mb-6">
        <FormProduct />
      </section>
      <section class="flex gap-4 items-start">
        <!-- Tabla de Productos -->
        <article class="flex-2/3">
          <TableProducts :products="products" />
        </article>
        <!-- Producto seleccionado -->
        <article class="flex-1/3 border border-slate-200 rounded-xl p-6">
          <ActiveProduct product="Paleta" :quantity="20" />
        </article>
      </section>
    </div>
  </main>
</template>

<script setup lang="ts">
import FormProduct from '../components/FormProduct.vue'
import TableProducts from '../components/TableProducts.vue'
import ActiveProduct from '../components/ActiveProduct.vue'
import type { Product } from '../interfaces/product.interface'

const products: Product[] = [
  {
    id: '1',
    name: 'Paleta',
    description:
      'Descripcion de la paleta, descripcion de la paleta, <dddddd</dddddd>',
    quantity: 20,
    price: 100,
  },
]
</script>
