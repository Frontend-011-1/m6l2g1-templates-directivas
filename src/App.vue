<template>
  <main class="container">
    <h1 class="text-center">Probando Directivas Vue</h1>
    <UsersComponent />
  </main>
</template>

<script>
import UsersComponent from '@/components/UsersComponent.vue';

export default {
  name: 'component-name',
  // props: {},
  data: function () {
    return {

    }
  },
  // computed: {},
  //methods: {},
  // watch: {},
  components: {
    UsersComponent
  },
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
}
</script>

<style scoped></style>