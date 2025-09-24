<template>
  <div id="basicLayout">
    <a-layout style="min-height: 100vh; min-width: 100vw">
      <a-layout-header class="header">
        <GlobalHeader />
      </a-layout-header>
      <a-layout-content class="content">
        <router-view />
      </a-layout-content>
      <a-layout-footer class="footer"> Author:NieReol Project:Cloud Picture</a-layout-footer>
    </a-layout>
  </div>
</template>

<script setup lang="ts">
import GlobalHeader from '@/components/GlobalHeader.vue'
</script>

<style scoped>
#basicLayout .footer {
  background: #efefef;
  position: fixed;
  padding: 16px;
  bottom: 0;
  left: 0;
  right: 0;
  text-align: center;
}
#basicLayout .content {
  background: linear-gradient(to right, #fff, #ffffff);
  margin-bottom: 20px;
  padding: 20px;
}

#basicLayout .header {
  padding-inline: 20px;
  margin-bottom: 16px;
  background: #fff;
  color: unset;
}
</style>
