<template>
  <!-- Renderizado condicional v-if -->
  <!-- 0 falsy,  1,2,3,4 truthy -->
  <div v-if="usuarios.length">
    <h2>Lista de usuarios</h2>
    <ul class="list-group">
      <!-- Directiva v-for para recorrer iterables (array) -->
      <li class="list-group-item" v-for="usuario in usuarios" :key="usuario.nombre">Nombre: {{ usuario.nombre }} -
        Edad:
        {{ usuario.edad }}</li>
    </ul>
  </div>
  <p class="text-danger" v-else>No hay usuarios en la lista</p>
</template>

<script>
export default {
  name: 'UsersComponent',
  // props: {},
  data: function () {
    return {
      usuarios: [
        { nombre: 'Ana', edad: 28 },
        { nombre: 'Luis', edad: 34 },
        { nombre: 'María', edad: 22 },
        { nombre: 'Carlos', edad: 45 }
      ]
    }
  },
  // computed: {},
  //methods: {},
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
}
</script>

<style scoped></style>