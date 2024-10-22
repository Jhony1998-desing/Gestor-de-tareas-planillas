<template>
  <div id="app" class="container">
    <h1 class="my-4">Gestor de Tareas</h1>
    <AgregarTarea @nueva-tarea="agregarTarea"></AgregarTarea>
    <TareasDeAPI></TareasDeAPI>
    <VistaCombinada :tareas="tareas"></VistaCombinada>
  </div>
</template>

<script>
import AgregarTarea from './components/AgregarTarea.vue';
import TareasDeAPI from './components/TareasDeAPI.vue';
import VistaCombinada from './components/VistaCombinada.vue';

export default {
  components: {
    AgregarTarea,
    TareasDeAPI,
    VistaCombinada
  },
  data() {
    return {
      tareas: []
    };
  },
  methods: {
    agregarTarea(tarea) {
      this.tareas.push(tarea);
    }
  }
};
</script>
