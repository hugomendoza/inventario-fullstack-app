<template>
  <form>
    <div class="flex gap-4 mb-4">
      <fieldset class="flex-1">
        <label class="text-sm text-slate-600 mb-2" for="product"
          >Producto</label
        >
        <input
          id="product"
          name="product"
          type="text"
          placeholder="Nombre de producto"
          class="block border border-slate-200 rounded-lg p-2 w-full"
        />
      </fieldset>
      <fieldset class="flex-1">
        <label class="text-sm text-slate-600 mb-2" for="price">Precio</label>
        <input
          id="price"
          name="price"
          type="text"
          placeholder="Precio"
          class="block border border-slate-200 rounded-lg p-2 w-full"
          pattern="[0-9]*"
          maxlength="6"
        />
      </fieldset>
      <fieldset class="flex-1">
        <label class="text-sm text-slate-600 mb-2" for="quantity"
          >Cantidad</label
        >
        <input
          id="quantity"
          name="quantity"
          type="text"
          placeholder="Cantidad"
          class="block border border-slate-200 rounded-lg p-2 w-full"
          maxlength="5"
        />
      </fieldset>
    </div>
    <div class="flex gap-2">
      <fieldset class="flex-2/3">
        <label class="text-sm text-slate-600 mb-2" for="description"
          >Descripción</label
        >
        <textarea
          id="description"
          name="description"
          type="text"
          placeholder="Description"
          class="block border border-slate-200 rounded-lg p-2 w-full resize-none"
          rows="3"
        />
      </fieldset>
      <fieldset class="flex-1/3 px-4 pt-6">
        <button
          class="bg-indigo-500 hover:bg-indigo-600 text-white px-4 py-2 rounded-lg"
        >
          Guardar
        </button>
      </fieldset>
    </div>
  </form>
</template>
