<script setup lang="ts">
  import { formDate } from '@/utils/time';
  import { ref, Ref } from 'vue';
  import AppIcon from '@/components/AppIcon.vue';
  import { useRouter } from 'vue-router';
  let time: Ref<string> = ref(formDate(new Date().toISOString()));
  const router = useRouter();
  function goLogin() {
    router.push({ name: 'Login' });
  }
</script>

<template>
  <div class="layout">
    <img src="@/assets/images/head.jpg" alt="" />
    <a href="https://github.com/evilsfdd/MyTemplateByVite">
      <app-icon icon="mdi:github" class="text-5xl cursor-pointer"></app-icon>
    </a>
    <span class="text-green-100">给个star呗</span>
    <h2>
      {{ time }}
      <br />
    </h2>
    <div>环境：vite2+eslint+prettier</div>
    <div>语言:Vue3.2+Typescript+scss+h5</div>
    <div>生态：vue-router路由+pinia仓库</div>
    <div>TailWind CSS框架+ElementsUI-plus组件库+Iconfy图标库</div>
    <div>工具类（待增加）：dayjs+lodash</div>
    <button @click="goLogin">登录页</button>
  </div>
</template>

<style lang="scss" scoped>
  .layout {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  img {
    width: 30%;
  }
  h2 {
    font-size: 60px;
  }
  div {
    font-size: 20px;
  }
  button {
    width: 100px;
    height: 40px;
    background-color: #a2d2;
    border-radius: 30px;
  }
</style>
