<script setup lang="ts">
import IconBlog from './icons/IconBlog.vue';
import IconGithub from './icons/IconGithub.vue';
import IconJuejin from './icons/IconJuejin.vue';
function handleOpenLink(url: string) {
  window.open(url);
}
</script>

<template>
  <div class="my-header">
    <div class="left">
      <img class="logo text-middle" src="../assets/logo.PNG" alt="logo" />
      <span class="text-middle">封面宝</span>
    </div>
    <div class="right">
      <icon-blog class="link" @click="handleOpenLink('https://chendx97.github.io/blog/')" />
      <icon-github class="link" @click="handleOpenLink('https://github.com/chendx97')" />
      <icon-juejin class="link" @click="handleOpenLink('https://juejin.cn/user/638161460403287/posts')" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.my-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  padding: 0 20px;
  background-color: #fff;
  box-shadow: var(--el-box-shadow-lighter);

  .left {
    font-size: 18px;

    .logo {
      margin-right: 5px;
      width: 30px;
    }
  }

  .right {
    display: flex;
    align-items: center;
    gap: 15px;

    .link {
      padding: 5px;
      cursor: pointer;
    }
  }
}
</style>
