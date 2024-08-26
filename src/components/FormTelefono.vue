<script>
export default {
  name: 'FormTelefono',
  data() {
    return {
      telefono: ''
    }
  }
}
</script>
<template>
  <label for="telefono">Teléfono</label>
  <input type="text" id="telefono" v-model="telefono" />
  <p v-show="telefono && !telefonoValido">El número de teléfono solo debe contener dígitos</p>
</template>
<style scoped>
p {
  color: red;
}
</style>
