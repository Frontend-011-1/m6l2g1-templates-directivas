<template>
  <!-- Para formularios siempre ocuparemos v-model -->
  <!-- <form class="border rounded-3 p-4" v-on:submit.prevent="manejarSubmit"> -->
  <!-- Metodo abreviado v-on:evento = @evento -->
  <form class="border rounded-3 p-4" @submit.prevent="manejarSubmit">
    <div class="mb-3">
      <label for="email" class="form-label">Email</label>
      <input type="email" name="email" id="email" class="form-control" placeholder="Ej: juanin@mail.com"
        v-model="email">
    </div>
    <div class="mb-3">
      <label for="mensaje" class="form-label">Mensaje</label>
      <textarea class="form-control" name="mensaje" id="mensaje" v-model="mensaje"></textarea>
    </div>
    <button class="btn btn-primary" type="submit">Enviar</button>
  </form>
  <h2>{{ email }}</h2>
  <h2>{{ mensaje }}</h2>
</template>

<script>
export default {
  name: 'FormularioContacto',
  // props: {},
  data: function () {
    return {
      email: '',
      mensaje: '',
    }
  },
  // computed: {},
  methods: {
    manejarSubmit(event) {
      console.log(`${this.email} envió este mensaje:\n`)
      console.log(this.mensaje)
      // Limpiar formulario
      // event.target.reset()
      this.email = ''
      this.mensaje = ''
    },
  },
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
}
</script>

<style scoped></style>