<template>
<div class="login">
  <v-app>
    <v-app-bar app>
      <v-toolbar-title>SH Project</v-toolbar-title>
       <v-spacer></v-spacer>
          <v-spacer></v-spacer>
      <v-btn color="yellow" v-on:click="home">Home</v-btn>
    </v-app-bar>
    <v-app-main>
      <div class="main">
        <div class="mainimage">
          <v-img alt="Vue logo" src="../assets/image/main.jpg" id="img"></v-img>
        </div>
      </div>
     <v-content id="content">
      <v-card width="450" class="mx-auto mt-9">
        <v-card-text><p id="signuptitle">가입하기 - 프로필 정보</p></v-card-text>
        <v-card-text>
          <form action="" method="get">
          <div>이름*</div>
          <input type="text" class="input">
          <br>
          <div>회원 구분*</div>
          <input type="text" class="input">
          <br>
          <div>학교 또는 학원 이름 입력하기*</div>
          <input type="text" class="input">
          </form>
        </v-card-text>
        <v-card-actions>
          <v-btn type="submit" form="" color="yellow" id="nextbtn" >다음</v-btn>
        </v-card-actions>
        <br>
        <div id="footerbtn">
          이미 가입했다면? <v-btn text v-on:click="login">로그인하기</v-btn>
        </div>
        <br>
      </v-card>
    </v-content>
    </v-app-main>
  </v-app>
  </div>
</template>
<script>
export default {
  name:'Login',
  data() {
   return{
      showPassword:false
    }
  },
  methods: {
    home:function(){
      this.$router.push('/')
    },
     login:function(){
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
p{
  text-align: center;
  font-weight: bold;
}
#content{
  margin-top: 10%;
}
#signuptitle{
  font-size: 20px;
}
#nextbtn{
  margin-left: 45%;
}
#footerbtn{
  padding-left: 25%;
}

</style>