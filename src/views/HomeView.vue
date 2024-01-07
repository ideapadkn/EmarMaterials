<script setup>
import Navbar from '@/components/Navbar.vue';
import Sidebar from '@/components/Sidebar.vue';
import MainContent from '@/components/MainContent.vue';
</script>

<template>
  <div class="main">
    <Navbar />
    <div class="main-container flex gap-5">
      <Sidebar />
      <MainContent />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.main {
  &-container {
    margin-top: 24px;
  }
}
</style>