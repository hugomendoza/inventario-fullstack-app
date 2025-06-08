<template>
  <!-- formulario -->
  <main class="bg-slate-100 min-h-dvh p-4">
    <div class="max-w-6xl mx-auto bg-white rounded-2xl p-6 shadow-md">
      <section class="border border-slate-200 rounded-lg p-6">
        <FormProduct />
      </section>
      <section>
        <!-- Tabla de Productos -->
        <article>
          <TableProducts />
        </article>
        <!-- Producto seleccionado -->
        <article>
          <ActiveProduct />
        </article>
      </section>
    </div>
  </main>
</template>

<script setup lang="ts">
import FormProduct from '../components/FormProduct.vue'
import TableProducts from '../components/TableProducts.vue'
import ActiveProduct from '../components/ActiveProduct.vue'
</script>
