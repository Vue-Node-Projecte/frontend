<template>
  <div class="home">
    <v-app>
       <v-app-bar app>
      <v-toolbar-title>SH Project</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color="yellow" v-on:click="start">시작하기</v-btn>
    </v-app-bar>
    <v-main>
      <v-img alt="Vue logo" src="../assets/image/main.jpg" id="img"></v-img>
    </v-main>
    </v-app>
  </div>
</template>

<script>
export default {
  name:'Home',
  methods: {
    start:function(){
      this.$router.push('/login')
    }
  },
}
</script>
<style>
  #img{
  position: fixed; 
  top: 0; 
  left: 0; 
  min-width: 100%;
  min-height: 100%;
}
</style>