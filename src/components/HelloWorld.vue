<script setup lang="ts">
import { ref } from "vue";
import { ElMessage } from "element-plus";

defineProps<{ msg: string }>();

const count = ref(0);
const input = ref("element-plus");

const curDate = ref("");

const toast = () => {
  ElMessage.success("Hello");
};

const value1 = ref(true);
</script>

<template>
  <h1 color="$ep-color-primary">{{ msg }}</h1>

  <div class="mb-4">
    <el-button size="large" @click="toast">El Message</el-button>
  </div>
</template>





<style>
.ep-button {
  margin: 4px;
}
.ep-button + .ep-button {
  margin-left: 0;
  margin: 4px;
}
</style>



