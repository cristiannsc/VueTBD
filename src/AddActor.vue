<template>
  <div class="center">
    <h2>{{title}}</h2>
    
      <p>
        <label for="firstName">Nombre</label>
        <input type="text" id="firstName" name="firstName" v-model="actor.firstName" onClick="this.select();">
      </p>
      <p>
        <label for="lastName">Apellido</label>
        <input type="text" id="lastName" name="lastName" v-model="actor.lastName" onClick="this.select();">
      </p>
      <p><button v-on:click="addActor()">Agregar Actor</button></p>
    
  </div>
</template>

<script>
  export default {
    data(){
      return{
        title:'Agregar actor',
        actor:{firstName:'',lastName:''}
      }
    },
    methods:{
      addActor:function(){
        this.$http.post('http://localhost:8080/TallerSakilaTBD/actors', this.actor)
      }
    }
  }
</script>
