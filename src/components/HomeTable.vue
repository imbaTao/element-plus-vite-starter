<template>
  <el-image
    :src="wallPapper"
    alt="Full Page Image"
    class="full-width-image"/>
  
    <el-table :data="items" style="width: 100%">
        <el-table-column prop="name" label="名称" width="120">

        </el-table-column>

        <el-table-column prop="name" label="链接" width="120">
            <template #default="{ row }">
                <a :href="row.url" target="_blank">{{ row.url }}</a>
            </template>
        </el-table-column>
    </el-table>
</template>

<script>
export default {
  data() {
    return {
      wallPapper:
        "https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg",
      scale: 1.0,
      items: [
        {
            name: "百度",
            url: "https://www.baidu.com"
        }
        ,
        {
            name: "element-plus",
            url: "https://element-plus.org/zh-CN/component/select-v2.html"
        }
      ]
    };
  },
};
</script>

<style>
/* 设置 body 和 html 的高度为 100% */
body,
html {
  height: 100%;
  margin: 0;
  padding: 0;
}

/* 设置图片的样式，铺满整个页面 */
img {
  width: 100%;
  height: 100%;
  object-fit: cover; /* 使用 cover 让图片铺满整个页面，并保持宽高比例 */
}

.full-width-image {
  width: 100vw; /* 设置图片的宽度为屏幕宽度 */
  height: 240px; /* 根据宽度等比例缩放高度 */
}
</style>
