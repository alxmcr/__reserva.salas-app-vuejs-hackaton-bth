<template>
<div id="app">
  <div class="titles">
    <h1 class="title-1">{{ titleApp }}</h1>
    <h2 class="title-2">{{ subtitleApp }}</h2>
  </div>
  <login-form></login-form>
</div>
</template>

<script>
import LoginForm from './components/LoginForm';

export default {
  name: 'app',
  components: {
    LoginForm
  },
  data(){
    return {
      titleApp: 'SSAL',
      subtitleApp: 'Sistema de reservación de salas'
    }
  }
}

</script>

<style lang="scss">
@import 'assets/scss/main.scss';

.titles{
  margin: 20px 0;
  padding: 10px;
}
</style>
