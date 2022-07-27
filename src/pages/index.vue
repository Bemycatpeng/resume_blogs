<template>
  <div class="bg-slate-500 text-4xl">我是首页</div>
</template>

<script lang="ts">
  import { defineComponent, onMounted } from 'vue';

  export default defineComponent({
    name: 'IndexPage',

    setup() {
      const test = () => {
        console.log('我是模板加载');
      };
      onMounted(() => {
        test();
      });
    }
  });
</script>
