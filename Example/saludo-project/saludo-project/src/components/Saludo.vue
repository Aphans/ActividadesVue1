<template>
  <h1>{{ nombre }}</h1>
  <h1>{{ apellido }}</h1>
</template>
<script>
export default {
  name: "Saludo",
  props: {
    nombre: {
      type: String,
      required: true,
    },
    apellido: {
      type: String,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>
