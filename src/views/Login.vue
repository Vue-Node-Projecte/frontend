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
        <v-card-text><p id="logintitle">시작하기</p></v-card-text>
        <v-card-text><p>환영합니다! 계정이 없다면 회원가입 후 이용해주세요.</p></v-card-text>
        <v-card-text>
          <div>이메일 주소*</div>
          <v-text-field prepend-icon="mdi-email" name="email" v-model="email" label="이메일" type="email" ></v-text-field>
          <div>비밀번호*</div>
          <v-text-field 
          label="비밀번호" 
          name="password"
          :type="showPassword ? 'text' : 'password'"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"/>
        </v-card-text>
        <v-card-actions>
          <v-btn type="submit" form="" color="yellow" id="loginbtn" >로그인</v-btn>
        </v-card-actions>
        <br>
        <div id="footerbtn">
          <v-btn text v-on:click="passwordfind">비밀번호 찾기</v-btn>
          <v-btn text v-on:click="signup">가입하기</v-btn>
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
    signup:function(){
      this.$router.push('/signup')
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
#logintitle{
  font-size: 20px;
}
#loginbtn{
  margin-left: 45%;
}
#footerbtn{
  padding-left: 25%;
}
</style>