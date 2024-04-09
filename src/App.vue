
<template>
  <el-config-provider namespace="ep",locale="locale",message="config">
    <!-- <BaseHeader /> -->
    <!-- <div class="flex main-container"> -->
      <!-- <BaseSide /> -->
      <!-- <div w="full" py="4"> -->
        <!-- <HelloWorld msg="快捷启动" /> -->
        <HomeTable/>
      <!-- </div> -->
    <!-- </div> -->
  </el-config-provider>
</template>



<style>
#app {
  text-align: start;
  color: var(--ep-text-color-primary);
}

.main-container {
  height: calc(100vh - var(--ep-menu-item-height) - 3px);
}
</style>


<script lang="ts" setup>
import { reactive } from 'vue'
import { ElMessage } from 'element-plus'
import { computed, ref } from 'vue'
import zhCn from 'element-plus/es/locale/lang/zh-cn'
import en from 'element-plus/es/locale/lang/en'

const language = ref('zh-cn')
const locale = computed(() => (zhCn))

const open = () => {
  ElMessage('This is a message.')
}
</script>