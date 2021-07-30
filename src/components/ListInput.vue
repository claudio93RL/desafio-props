<template>
  <div>
    <label class="font-weight-bold">Tarea:</label>
    <input
      class="mx-3"
      type="text"
      v-model="nuevaTarea"
      placeholder="Ingrese nueva tarea"
    />
    <button class="btn btn-info" @click="agregarTarea">Añade</button>
  </div>
</template>

<script>
export default {
  name: "ListInput",
  data() {
    return {
      nuevaTarea: "",
    };
  },
  methods: {
    agregarTarea() {
      this.$emit("nuevasTareas", this.nuevaTarea);
      this.nuevaTarea = "";
    },
  },
};
</script>

<style>
</style>