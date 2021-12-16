<template>
  <div id="app" class="container">
    <div class="bg-secondary text-white rounded">
      <span>
        {{ objeto.mensaje | mayusculas }}
      </span>
      <hr>
      <span>
        {{ objeto.mensaje | suspensivos | mayusculas}}
      </span>
      <hr>
      <span>
        {{ objeto.temperatura | aFa}}
      </span>
      <hr>
      <span>
        {{objeto.numero | sumarcinco}}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      objeto: {
        mensaje: 'Hola este es el mensaje, aprende vuejs',
        temperatura : 20,
        numero: 5
      }      
    }
  },
  filters: {
    mayusculas(mensaje){
      return  mensaje.toUpperCase();
    },
    aFa(temperatura){
      return (9/5 * temperatura) + 32 + ' F'
    }
  }
}
</script>

<style>

</style>
