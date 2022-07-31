<template>
  <!-- 头部侧边栏/侧边栏 -->
  <SideBar />
  <MainContent class="tw-mt-4" />
  <NavBar />
</template>

<script lang="ts">
  import { defineComponent, onMounted } from 'vue';

  import SideBar from '@/components/SideBar.vue';
  import MainContent from '@/components/MainContent.vue';
  import NavBar from '@/components/NavBar.vue';

  export default defineComponent({
    name: 'IndexPage',
    components: {
      SideBar,
      MainContent,
      NavBar
    },

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
