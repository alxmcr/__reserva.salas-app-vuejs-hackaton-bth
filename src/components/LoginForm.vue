<template>
    <div id="login">
        <form action="" v-on:submit.prevent="enviarDatos" id="form-login">
            <div class="form-inputs">
                <label for="username" class="form-label">USERNAME:</label>
                <input v-model="username" type="text" name="username" id="username" class="form-input">
                <label for="password" class="form-label">PASSWORD:</label>
                <input v-model="password" type="password" name="password" id="password" class="form-input">   
            </div>
            <div v-if="infoLoginCompleta" class="form-botones">
                <input type="submit" value="Ingresar" class="form-boton">
                <input type="reset" value="Limpiar" class="form-boton">
            </div>  
        </form>
        <pre class="info">
        {{ $data }}
        </pre>
    </div>
</template>

<script>

export default {
  name: 'login',

  data() {
      return {
        username: '',
        password: ''
      }
  }, 

  methods: {
      enviarDatos: function(){
          alert("Enviando los datos...");
          this.username = '';
          this.password = '';
      }
  }, 

   computed: {
        infoLoginCompleta: function () {
            if (this.username && this.password){
                return true;
            }
            return false;
        }
    }
}
</script>

<style lang="scss">
.info{
    background-color: red;
}
</style>

