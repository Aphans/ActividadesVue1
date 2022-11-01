<!-- eslint-disable prettier/prettier -->
<template>
  <div>
    <form id="myform" @submit="validateForm">
    <label>Escribe tu nombre:</label><br>
    <input type="text" v-model="Nombre" placeholder="Escribe tu nombre" /> <br>
    <label>Escribe tus apellidos:</label><br>
    <input type="text" v-model="Apellidos" placeholder="Escribe tus apellidos" />
    <input type="submit" value="Enviar"/>
    </form>
    <h1>Hola {{Nombre}} {{Apellidos}}</h1>
    <h1 id="Mensaje">{{Message}}</h1>
  </div>
</template>
<script>
export default {
  name: "myForm",
  data() {
    return {
      Nombre: "",
      Apellidos: "",
      Message: "",
    };
  },
  methods: {
    validateForm: function (e) {
      if (!this.Nombre) {
        this.Message = "Debes introducir el nombre";
        e.preventDefault();
      }
      if (!this.Apellidos) {
        this.Message = "Debes introducir los apellidos";
        e.preventDefault();
      }
    },
  },
};
</script>
