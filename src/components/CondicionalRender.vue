<script>
export default {
  nombre: 'ConditionalRender',
  data() {
    return {
      isVisibleVIF: true,
      isVisibleVShow: true
    }
  }
}
</script>
<template>
  <h1>Renderizado condicional</h1>

  <h2>Renderizado v-if</h2>
  <input type="checkbox" v-model="isVisibleVIF" />
  <img
    src="https://laderasur.com/wp-content/uploads/2017/11/h4777-3.jpg"
    alt=""
    v-if="isVisibleVIF"
  />

  <p v-else>Lamentablemente, no podemos mostrar tu imagen</p>

  <h2>Renderizado v-show</h2>

  <img
    src="https://laderasur.com/wp-content/uploads/2017/11/h4777-3.jpg"
    alt=""
    v-show="isVisibleVShow"
  />
</template>
<style scoped></style>
