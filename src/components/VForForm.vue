<script>
export default {
  name: 'VForForm',
  data() {
    return {
      selectedOption: '',
      /** Los SKU son únicos */
      optionsForm: [
        { sku: 'martillo-ASDJ12W3', nombre: 'Martillo' },
        { sku: 'sierra-ASDJ22W3', nombre: 'Sierra' },
        { sku: 'clavos-ASDJ32W3', nombre: 'Clavos' },
        { sku: 'serrucho-ASDJ42W3', nombre: 'Serrucho' }
      ]
    }
  }
}
</script>
<template>
  <label for="productos">Selecciona un producto</label>
  <select v-model="selectedOption" id="productos">
    <option v-for="producto in optionsForm" :key="producto.sku" :value="producto.sku">
      {{ producto.nombre }}
    </option>
  </select>
</template>
<style></style>
