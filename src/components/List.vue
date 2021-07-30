<template>
  <div
    class="d-flex justify-content-center flex-column align-items-center py-5"
  >
    <ListInput @nuevasTareas="agregarTarea" />
    <ListItems :tareas="tareas" />
  </div>
</template>

<script>
import ListInput from "./ListInput.vue";
import ListItems from "./ListItems.vue";

export default {
  components: {
    ListInput,
    ListItems,
  },
  data() {
    return {
      tareas: [],
    };
  },
  methods: {
    agregarTarea(tarea) {
      this.tareas.push(tarea);
      this.nuevaTarea = "";
    },
  },
};
</script>

<style>
</style>