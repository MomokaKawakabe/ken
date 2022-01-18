<template>
  <div class="page-login">
    <div class="login-dialog">
      <div class="content-logo">
        <div class="login-title">
          登录
        </div>
      </div>
      <div class="grey-line" />
      <div class="login-phone">
        <div class="content-phone">
          <div class="phone-logo" />
        </div>
        <input v-model="phone" type="text" class="phone el-input__inner" placeholder="手机号" @keyup.enter="login">
      </div>
      <div class="login-password">
        <div class="content-password">
          <div class="password-logo" />
        </div>
        <input v-model="password" type="password" class="password el-input__inner" placeholder="密码" @keyup.enter="login">
      </div>

      <div class="dialog-button">
        <div class="login-but">
          <button class="default-button w270 login" @click="login">
            登录
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Vue from 'vue'
export default Vue.extend({
  name: 'PageLogin',
  data () {
    return {
      password: '',
      phone: ''
    }
  },
  methods: {
    login () {
      console.log('登录！')
    }
  }
})
</script>
<style lang="less" rel="stylesheet/less">
@import "assets/css/color";
.page-login{
  width: 100%;
  height:100%;
  background: url('static/img/background.png') 50% 50% no-repeat;
  background-size: cover;
  padding-top: 290px;
  .login-dialog{
    width: 409px;
    height: 300px;
    margin: auto;
    background-color: @b_panel;
    position: relative;
    .content-logo{
      width: 100%;
      padding: 16px 87px;
      .login-title{
        color: @f_main_blue;
        font-size: 28px;
        font-weight: bolder;
      }
    }
    .login-phone{
      margin-top: 28px;
      width: 100%;
      height:42px;
      text-align: center;
      padding: 0 20px;
      .content-phone{
        position: absolute;
        background-color: #f2f8fe;
        width: 36px;
        height: 40px;
        display: inline-block;
        padding: 8px;
        .phone-logo{
          background: url('static/img/phone.png') center;
          background-repeat: no-repeat !important;
          background-size: contain;
          height:100%;
          width: 100%;
        }
      }
      .phone{
        margin-left: 36px;
        display: inline-block;
        height:40px;
        width: 80%;
      }
      .el-input__inner{
        -webkit-appearance: none;
        background-color: #f2f8fe;
        border-radius: 0;
        border: 1px solid #f2f8fe;
        box-sizing: border-box;
        color: #606266;
        display: inline-block;
        font-size: inherit;
        height: 40px;
        line-height: 36px;
        outline: 0;
        padding: 0 15px;
        -webkit-transition: border-color .2s cubic-bezier(.645,.045,.355,1);
        transition: border-color .2s cubic-bezier(.645,.045,.355,1);
        width: 80%;
      }
    }
    .login-password{
      margin-top: 17px;
      width: 100%;
      height:42px;
      text-align: center;
      padding: 0 20px;
      .content-password{
        position: absolute;
        background-color: #f2f8fe;
        width: 36px;
        height: 40px;
        display: inline-block;
        padding: 8px;
        .password-logo{
          background: url('static/img/password.png') center;
          background-repeat: no-repeat !important;
          background-size: contain;
          height:100%;
          width: 100%;
        }
      }
      .password{
        margin-left: 36px;
        display: inline-block;
        height:40px;
        width: 80%;
      }
      .el-input__inner{
        -webkit-appearance: none;
        background-color: #f2f8fe !important;
        border-radius: 0;
        border: 1px solid #f2f8fe;
        box-sizing: border-box;
        color: #606266;
        display: inline-block;
        font-size: inherit;
        height: 40px;
        line-height: 36px;
        outline: 0;
        padding: 0 15px;
        -webkit-transition: border-color .2s cubic-bezier(.645,.045,.355,1);
        transition: border-color .2s cubic-bezier(.645,.045,.355,1);
        width: 80%;
      }
    }
    .dialog-button{
      margin-top: 24px;
      width: 100%;
      height: auto;
      text-align: center;
      .login-but{
        display: inline-block;
        .login{
          color: #ffffff;
          font-size: 16px;
          height: 36px;
          width:270px;
          background-color: #4275d8;
        }
      }
      .register-but{
        display: inline-block;
        margin-left: 20px;
        .register{
          color: #ffffff;
          font-size: 16px;
          height: 36px;
          width: 129px;
          background-color: #f7931e;
        }
      }
    }
    .forget-password{
      position: absolute;
      margin-top: 20px;
      right: 25px;
      .password-text{
        color: #4275d8;
        font-size: 16px;
        cursor: pointer;
      }
    }
  }
}
</style>
