<template>
  <div class="center">
    <h2>{{title}}</h2>
    <form action="http://localhost:8081/sakila-tbd" method="POST">
      <p>
        <label for="firstName">Nombre</label>
        <input type="text" id="firstName" name="firstName" value="Ej.: Tom" onClick="this.select();">
      </p>
      <p>
        <label for="lastName">Apellido</label>
        <input type="text" id="lastName" name="lastName" value="Ej.: Hanks" onClick="this.select();">
      </p>
      <p><input type="submit" value="Agregar actor"></button></p>
    </form>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        title:'Agregar actor',
      }
    },
    mounted:function(){
      console.log('Index.vue');
    }
  }
</script>
