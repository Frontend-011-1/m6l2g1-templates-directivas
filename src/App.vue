<template>
  <Navbar />
  <main class="container my-4">
    <h1 class="text-center" @click="manejarClickH1">Probando Directivas Vue</h1>
    <!-- <UsersComponent /> -->

    <section class="my-4">
      <ul class="nav nav-tabs">
        <!-- Por cada tab que tengamos guardado en el array de tabs -->
        <!-- (el nombre de cada tab es el nombre exacto de cada componente) -->
        <li class="nav-item" v-for="tab in tabs" :key="tab" @click="tabSeleccionada = tab">
          <a class="nav-link">{{ tab }}</a>
        </li>
      </ul>

      <KeepAlive>
        <component :is="tabSeleccionada"></component>
      </KeepAlive>

    </section>

    <!-- Probando detención de propagación de un evento click -->
    <!-- Usando modificador .stop -->
    <div class="propagation2 my-4" @click="alertDiv2">
      div2
      <div class="propagation1" @click.stop="alertDiv1">
        div1
      </div>
    </div>

    <!-- <Mostrar /> -->
  </main>
</template>

<script>
import UsersComponent from '@/components/UsersComponent.vue';
import Navbar from './components/Navbar.vue';
import Mostrar from './components/Mostrar.vue';
import FormularioContacto from './components/FormularioContacto.vue';

export default {
  name: 'App',
  // props: {},
  data: function () {
    return {
      tabs: ['UsersComponent', 'Mostrar', 'FormularioContacto'],
      tabSeleccionada: 'UsersComponent'
    }
  },
  // computed: {},
  methods: {
    manejarClickH1() {
      console.log('Hizo click en el H1!!!')
    },
    alertDiv1() {
      alert('Click en div 1')
    },
    alertDiv2() {
      alert('Click en div 2')
    }
  },
  // watch: {},
  components: {
    UsersComponent,
    Navbar,
    Mostrar,
    FormularioContacto
  },
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
}
</script>

<style scoped>
.propagation2 {
  width: 200px;
  height: 200px;
  background-color: lightblue;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
}

.propagation1 {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
}
</style>