<script>
export default {
  name: 'MayorVeintiuno',
  data() {
    return {
      edad: ''
    }
  }
}
</script>

<template>
  <form>
    <label for="edad">Edad</label>
    <input type="number" id="edad" v-model="edad" />
    <p v-show="edad && edad < 21">Debes tener al menos 21 años</p>
    <button type="submit" :disabled="edad < 21">Enviar</button>
  </form>
</template>

<style scoped>
p {
  color: red;
}
</style>
