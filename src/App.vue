<template>
  <div id="app">
    <md-toolbar class="md-primary" md-elevation="1">
      <h3 class="md-title">GAME</h3>
      <span style="width:10px"></span>
      <span style="flex: 1"></span>
      <span style="flex: 1"></span>
      <div></div>
    </md-toolbar>
        <home/>
  </div>
</template>


<script>
import home from './views/Home'
export default {
  components:{
    home
  }
}
</script>

<style>
#app{
  text-align:center;
}
#buttonHome{
   margin-right:8px;
}
#buttonabout{
  margin-left:8px;
}
</style>
