<template>
  <div class="about">
    <h1>Formulario</h1>
    <form @submit.prevent="enviar">
      <label for="nombre">Nombre</label>
      <input 
        type="text" 
        placeholder="nombre"
        v-model.trim="tarea.nombre"
      >
      <br>
      <label for="tecnologías">React.js</label>
      <input 
        type="checkbox"
        id="react"
        v-model="tarea.tecnologia"
        value="react"
      >
      <label for="tecnologías">Vue.js</label>
      <input 
        type="checkbox"
        id="vue"
        v-model="tarea.tecnologia"
        value="vue"
      >
      <button type="submit" :disabled="bloquear">Enviar</button>
    </form>
    <hr>
    <h2>Resultado</h2>
    <p>{{tarea.nombre}}</p>
    <p>{{tarea.tecnologia}}</p>
    <div>
      {{respuesta.nombre}}
      {{respuesta.tecnologia}}
    </div>
  </div>
</template>

<script>
  export default {
    name: 'About',
    data() {
      return {
        tarea: {
          nombre: '',
          tecnologia: []
        },
        respuesta: {}
      }
    },
    methods: {
      enviar() {
        this.respuesta = this.tarea
        this.tarea = {
          nombre: '',
          tecnologia: []
        }
      }
    },
    computed: {
      bloquear() {
        return this.tarea.nombre.trim() === "" ? true : false
      }
    }
  }

</script>

