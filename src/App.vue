<template>
  <div id="app">
    <md-toolbar class="md-primary" md-elevation="1">
      <h3 class="md-title">GAME</h3>
    </md-toolbar>
    <home />
  </div>
</template>


<script>
import home from "./views/Home";
export default {
  components: {
    home
  }
};
</script>

<style>
#app {
  text-align: center;
  width: 100%;
  overflow-x: hidden;
}
#buttonHome {
  margin-right: 8px;
}
#buttonabout {
  margin-left: 8px;
}
.md-toolbar {
  width: 100%;
  margin: none;
  box-sizing: border-box;
}
</style>
