<template>
  <div class="home">
    <br>
    <br>
    <p>Form de Element ui</p>
    <!-- <form @submit.prevent="enviar">
        <h2>Input</h2>
        <el-input 
          placeholder="Please input" 
          v-model="tarea.nombre"
          class="input"
          size="small"
        ></el-input>
        <br>
        <h2>Checkbox</h2>
        <el-checkbox 
          v-model="tarea.opcion"
          label="Opción A"
        >
        </el-checkbox>
        <el-checkbox 
          v-model.trim="tarea.opcion"
          label="Opción B"
        >
        </el-checkbox>
        <br>
        <h2>Radio</h2>
        <el-radio v-model="tarea.radio" label="1">Option A</el-radio>
        <el-radio v-model="tarea.radio" label="2">Option B</el-radio>
        <br>
        <h2>number</h2>
        <el-input-number 
          v-model="tarea.num" 
          controls-position="right" 
          @change="handleChange" 
        ></el-input-number>
        <hr>
        <el-button type="primary">Enviar</el-button>
    </form>
    <p>{{tarea.nombre}}</p>
    <p>{{tarea.opcion}}</p>
    <p>{{tarea.radio}}</p> -->
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      tarea: {
        nombre: '',
        opcion: [],
        radio: '',
        num: 1
      }
    }
  },
  methods: {
      handleChange(value) {
    },
    enviar() {
      console.log(this.tarea)
    }
  }
}
</script>

<style scoped>
  .input{
    max-width: 300px;
  }
</style>
