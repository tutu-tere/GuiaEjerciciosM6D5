<script>
export default {
  name: 'RequisitosCheck',
  data() {
    return {
      requisitos: [
        { id: 1, texto: 'Dormí 8 horas', marcado: false },
        { id: 2, texto: 'Tomé 8 vasos de Agua', marcado: false },
        { id: 3, texto: 'Consumí los nutrientes que me recomendó el doctor', marcado: false }
      ]
    }
  },
  computed: {
    todosMarcados() {
      return this.requisitos.every((requisito) => requisito.marcado)
    }
  }
}
</script>

<template>
  <form>
    <div v-for="requisito in requisitos" :key="requisito.id">
      <input type="checkbox" v-model="requisito.marcado" />
      <label>{{ requisito.texto }}</label>
    </div>

    <p v-show="!todosMarcados" style="color: red">Debes cumplir con todos los requisitos</p>
    <button type="submit" :disabled="!todosMarcados">Enviar</button>
  </form>
</template>

<style scoped>
p {
  color: red;
}
</style>
