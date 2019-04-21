<template>
  <div class="login">
    <div class="loginWrapper">
      <h2>账号密码登录</h2>
      <a-divider />
      <a-input v-model="username" class="form-input" placeholder="输入用户名">
        <a-icon slot="prefix" type="user" />
      </a-input>
      <a-input v-model="password" class="form-input" placeholder="输入密码">
        <a-icon slot="prefix" type="lock" />
      </a-input>
      <a-button class="submit-btn" type="primary" @click="submit"
        >登录</a-button
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  components: {},
  data() {
    return {
      username: '',
      password: ''
    }
  },
  watch: {},
  created() {},
  mounted() {},
  methods: {
    submit() {
      if (!this.username || !this.password) {
        console.log('报错了')
      }
      console.log(this.username)
    }
  }
}
</script>

<style scoped>
.login {
  position: absolute;
  left: 0;
  top: 0;
  width: 100vw;
  height: 100vh;
  background: #f0f2f5 url('./../assets/image/login-bg.svg');
}

.loginWrapper {
  margin-left: 50%;
  margin-top: 20%;
  padding: 10px;
  width: 300px;
  text-align: center;
  transform: translate3d(-50%, -50%, 0);
}
.form-input {
  margin: 10px auto;
  height: 40px;
  font-size: 16px;
}
.submit-btn {
  width: 100%;
  margin-top: 10px;
  height: 40px;
}
</style>
