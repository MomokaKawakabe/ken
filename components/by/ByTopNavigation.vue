<template>
  <div class="top-navigation-bar">
    <div class="top-navigation-bar-logo-word">
      <div>
        上津未原
      </div>
    </div>
    <div class="top-navigation-bar-quit">
      <i class="el-icon-switch-button top-navigation-bar-quit-word" title="退出" @click.prevent="logout()" />
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    logout () {
      this.$router.push('/login')
    }
  }
}
</script>
<style lang="less" rel="stylesheet/less">
@import "assets/css/color";
.top-navigation-bar {
  height: 75px;
  // #3a4759 #505D58 #000000
  background-color: #ffffff;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  padding: 0 20px;
  color: @b_backplane;
  display: flex;
  justify-content: space-between;
  border-bottom: @b_theme_line solid 1px;
  .top-navigation-bar-logo-word {
    color: @f_main;
    font-size: 20px;
    line-height: 75px;
    padding-left: 20px;
  }
  .top-navigation-bar-quit {
    line-height: 75px;
    cursor: pointer;
    color: @button_main;
    .top-navigation-bar-quit-word {
      padding-right: 5px;
      &:hover {
        color: @button_main_active;
        cursor: pointer;
      }
    }
  }
}
</style>
