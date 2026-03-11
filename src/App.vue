<template>
  <h1> Nuevo Componente</h1>
</template>

<script>
export default {
  name: 'component-name',
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