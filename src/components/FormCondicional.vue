<script>
export default {
  name: 'FormCondicional',
  data() {
    return {
      email: ''
    }
  }
}
</script>
<template>
  <form>
    <label for="email">Email</label>
    <input type="email" id="email" v-model="email" />
    <p v-show="!email.includes('@')">Debes incluir un "@" en el correo</p>
    <button type="submit">Enviar</button>
  </form>
</template>
<style scoped>
p {
  color: red;
}
</style>
