<template>
  <div class="home">
    <!-- <Login  v-on:update-currentUser="updateCurrentUser" v-if="userCheck == false"/> -->
    <three />
    <!-- v-if="userCheck == true" -->
  </div>
</template>

<script>
// @ is an alias to /src
// import Login from "../components/Login.vue";
import three from "../components/three";

export default {
  name: "home",
  data() {
    return {
      // userCheck: false,
      // userul: ""
    };
  },
  components: {
    three
  }
  // methods: {
    // updateCurrentUser(user) {
    //   this.$emit("update-currentUser", user);
    //   this.checkUser(user);
    //   this.userul = user;
    // },
  //   checkUser(u) {
  //     if (u) this.userCheck = true;
  //   }
  // },
  // beforeMount() {
  //   if (this.userul != "Please Login") {
  //     alert("created if thern")
  //     this.userCheck = true;
  //   }else {this.userCheck = false
  //     alert("created if else")}
  // }
}
</script>

<style scoped>
</style>
