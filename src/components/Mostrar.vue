<template>
  <div v-show="mostrar" class="mb-4">
    <h2 class="display-2">Me ven?</h2>
  </div>
  <button class="btn btn-warning" @click="mostrar = !mostrar">{{ mostrar ? 'Ocultar' : 'Mostrar' }}</button>
</template>

<script>
export default {
  name: 'Mostrar',
  // props: {},
  data: function () {
    return {
      mostrar: true
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