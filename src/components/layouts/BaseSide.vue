<template>
  <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px">
    <el-radio-button :value="false">expand</el-radio-button>
    <el-radio-button :value="true">collapse</el-radio-button>
  </el-radio-group> -->
  <el-menu
    default-active="2"
    class="el-menu-vertical-demo"
    :collapse="false"
    @open="handleOpen"
    @close="handleClose"
  >
    <el-sub-menu index="1">
      <template #title>
        <el-icon><UserFilled /></el-icon>
        <p>用户管理</p>
      </template>

      
      <el-menu-item-group>
        <el-menu-item index="1-1">用户列表</el-menu-item>
        <el-menu-item index="1-2">邀请码变更</el-menu-item>
      </el-menu-item-group>
    </el-sub-menu>

    <el-sub-menu index="2">
      <template #title>
        <el-icon><Money /></el-icon>
        <p>财务管理</p>
      </template>

      
      <el-menu-item-group>
        <el-menu-item index="2-1">提现列表</el-menu-item>
        <el-menu-item index="2-2">充值列表</el-menu-item>
      </el-menu-item-group>
    </el-sub-menu>

    <!-- <el-menu-item index="2"> -->
      <!-- <el-icon><icon-menu /></el-icon>
      <template #title>Navigator Two</template>
    </el-menu-item>
    <el-menu-item index="3" disabled>
      <el-icon><document /></el-icon>
      <template #title>Navigator Three</template>
    </el-menu-item>
    <el-menu-item index="4">
      <el-icon><setting /></el-icon>
      <template #title>Navigator Four</template>
    </el-menu-item> -->
  </el-menu>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue'
import { userInfo } from 'os'

const isCollapse = ref(true)
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
</script>

<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>
