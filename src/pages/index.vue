<template>
  <!-- 头部侧边栏/侧边栏 -->
  <div></div>
</template>

<script lang="ts">
  import { defineComponent, onMounted } from 'vue';

  export default defineComponent({
    name: 'IndexPage',

    setup() {
      const test = () => {
        console.log('我是首页');
      };
      onMounted(() => {
        test();
      });
    }
  });
</script>
