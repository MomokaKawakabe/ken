<template>
  <div id="body">
    <div>
      <ByTopNavigation />
      <div id="page-wrapper" class="show-drawer">
        <nuxt-child />
      </div>
      <BySideNavigation />
    </div>
  </div>
</template>
<script>

export default {
  name: 'ByIndex',
  transition: 'fade',
  data () {
    return {
    }
  },
  watch: {
  },
  beforeMount () {
  },
  methods: {
  }
}
</script>
<style lang="less" rel="stylesheet/less">
#page-wrapper {
  position: fixed;
  left: 0;
  top: 75px;
  right: 0;
  bottom: 0;
  z-index: 90;
  overflow-y: auto;
  overflow-x: hidden;
  -webkit-transition: all 0.4s;
  -moz-transition: all 0.4s;
  -o-transition: all 0.4s;
  transition: all 0.4s;
  /*background-color: #f7f8fb;*/
  background-color: #F5F5F5;
  &.show-drawer {
    left: 225px;
  }
  &.show-drawer-isClick {
    left: 54px;
  }
}
</style>
