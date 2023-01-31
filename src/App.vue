<template>
  <el-config-provider :locale="lang">
    <router-view />
  </el-config-provider>
</template>

<script setup lang="ts">
import { reactive } from 'vue';
import { ElConfigProvider } from 'element-plus';
import zhCn from 'element-plus/es/locale/lang/zh-cn';
import en from 'element-plus/es/locale/lang/en';

const lang = reactive(localStorage.getItem('lang') === 'en' ? en : zhCn);
</script>

<style>
@import './assets/css/main.css';
@import './assets/css/color-dark.css';
</style>
