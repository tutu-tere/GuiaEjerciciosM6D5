<script>
export default {
  name: 'FormPass',
  data() {
    return {
      password: ''
    }
  }
}
</script>
<template>
  <form>
    <label for="password">Password</label>
    <input type="password" id="password" v-model="password" />
    <p v-show="password.length < 8">La contraseña debe tener al menos 8 caracteres</p>
    <button type="submit">Enviar</button>
  </form>
</template>
<style scoped>
p {
  color: red;
}
</style>
