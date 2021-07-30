<template>
  <ul class="mt-5">
    <li v-for="(item, $index) in tareas" :key="$index">
      <div class="d-flex justify-content-between align-items-center my-4">
        <p class="font-weight-bold d-inline mr-5 mb-0">{{ item }}</p>
        <button class="btn btn-danger" @click="EliminarTarea($index)">
          eliminar
        </button>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    tareas: {
      type: Array,
      default: () => {
        [];
      },
    },
  },
  methods: {
    EliminarTarea(index) {
      this.tareas.splice(index, 1);
    },
  },
};
</script>

<style>
</style>