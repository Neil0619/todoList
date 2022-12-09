<script lang="ts" setup>
import {ref} from 'vue'

import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue'

const isCollapse = ref(true)
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath)
}

</script>

<template><el-row class="tac">
  <el-col :span="12">
    <h5 class="mb-2">Custom colors</h5>
    <el-menu
      class="el-menu-vertical-demo"
      default-active="2"
      :collapse="isCollapse"
      @open="handleOpen"
      @close="handleClose"
    >
      <el-menu-item index="1">
          <el-icon><location /></el-icon>
          <span>今天</span>
      </el-menu-item>
      <el-menu-item index="2">
        <el-icon><icon-menu /></el-icon>
        <span>最近七天</span>
      </el-menu-item>
      <el-menu-item index="3">
        <el-icon><document /></el-icon>
        <span>指派给我</span>
      </el-menu-item>
      <el-menu-item index="4">
        <el-icon><setting /></el-icon>
        <span>收集箱</span>
      </el-menu-item>
    </el-menu>
    <el-divider />
  </el-col>
  <el-divider direction="vertical" />
  <el-col>

  </el-col>
</el-row>
</template>

<style scoped>
</style>
