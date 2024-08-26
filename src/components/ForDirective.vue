<script>
export default {
  nombre: 'ForDirective',
  data() {
    return {
      diasSemana: ['Lunes', 'Martes', 'Miercoles', 'Jueves', 'Viernes', 'Sabado', 'Domingo'],
      productos: [
        { sku: 'ASDJ12W3', nombre: 'Martillo' },
        { sku: 'ASDJ22W3', nombre: 'Sierra' },
        { sku: 'ASDJ32W3', nombre: 'Clavos' },
        { sku: 'ASDJ42W3', nombre: 'Serrucho' }
      ]
    }
  }
}
</script>
<template>
  <ul>
    <li v-for="(dia, idx) in diasSemana" :key="idx">{{ dia }}</li>
  </ul>

  <ul>
    <li v-for="producto in productos" :key="producto.sku">
      SKU:{{ producto.sku }} - Produto: {{ producto.nombre }}
    </li>
  </ul>
</template>
<style scoped></style>
