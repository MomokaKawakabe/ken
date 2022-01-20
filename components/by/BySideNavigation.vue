<template>
  <el-menu
    :default-active="activeIndex"
    class="side-navigation"
    background-color="#0061B4"
    text-color="#fff"
    active-text-color="#efc678"
  >
    <el-menu-item index="1" @click="$router.push('/by/article')">
      <i class="el-icon-edit-outline" />
      <span slot="title" class="title">写文章</span>
    </el-menu-item>
    <el-menu-item index="2" @click="$router.push('/by/article/list')">
      <i class="el-icon-notebook-2" />
      <span slot="title" class="title">文章列表</span>
    </el-menu-item>
  </el-menu>
</template>

<style lang="less" rel="stylesheet/less">
.side-navigation {
  position: fixed;
  top: 75px;
  bottom: 0;
  width: 225px;
  .title {
    font-size: 16px;
  }
}
</style>
