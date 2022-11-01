<template>
  <div><Nombre /><Apellidos /></div>
</template>
<script>
import Nombre from "./components/Nombre.vue";
import Apellidos from "./components/Apellidos.vue";
export default {
  components: { Nombre, Apellidos },
};
</script>
