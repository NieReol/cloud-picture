<template>
  <a-row :wrap="false">
    <a-col flex="100px" justify="center">
      <RouterLink to="/">
        <div class="title-bar">
          <img class="logo" src="@/assets/logo.png" alt="logo" />
          <div class="title">云图</div>
        </div>
      </RouterLink>
    </a-col>
    <a-col flex="auto">
      <a-menu v-model:selectedKeys="current" mode="horizontal" :items="items" />
    </a-col>
    <a-col flex="63px" justify="center">
      <div class="user-login-status">
        <a-button type="primary" href="/user/login">登录</a-button>
      </div>
    </a-col>
  </a-row>
</template>

<script lang="ts" setup>
import { h, ref } from 'vue'
import { AppstoreOutlined, HomeOutlined } from '@ant-design/icons-vue'
import type { MenuProps } from 'ant-design-vue'
import { RouterLink } from 'vue-router'
const current = ref<string[]>(['mail'])
const items = ref<MenuProps['items']>([
  {
    key: '/',
    icon: () => h(HomeOutlined),
    label: '主页',
    title: '主页',
  },
  {
    key: '/about',
    // icon: () => h(),
    label: '关于',
    title: '关于',
  },
  {
    key: 'others',
    icon: () => h(AppstoreOutlined),
    label: '其他',
    title: '其他',
  },
])
</script>
<style scoped>
.title-bar {
  display: flex;
  align-items: center;
}
.title {
  color: #1890ff;
  font-size: 18px;
  font-weight: bold;
}
.logo {
  width: 36px;
  height: 36px;
  vertical-align: middle;
}
</style>
