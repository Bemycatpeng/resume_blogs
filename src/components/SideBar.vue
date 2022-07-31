<template>
  <div
    class="tw-bg-card tw-p-4 tw-rounded-2xl tw-relative tw-overflow-hiddenfade-out-top"
    :class="iSopen ? 'h-[420px]' : 'h-[103px]'"
  >
    <!-- 向下展开的按钮 -->
    <div
      class="tw-text-main tw-bg-pink-300 tw-absolute tw-top-0 tw-right-0 tw-py-1 tw-px-2 tw-rounded-tr-lg tw-rounded-bl-lg"
      @click="switchDetails"
    >
      展开
    </div>

    <!-- 头像名称标签 -->
    <div class="tw-flex tw-flex-row">
      <div class="tw-w-20 tw-rounded-xl tw-bg-split">
        <img src="images/my-avatar.png" />
      </div>
      <div class="tw-ml-3 tw-flex tw-flex-col tw-justify-between tw-py-3">
        <span>刘鹏</span>
        <span class="tw-bg-slate-500 tw-px-2 tw-rounded-md tw-text-xs">Web developer</span>
      </div>
    </div>

    <!-- 信息详情模块 -->
    <div>
      <div class="tw-h-[1px] tw-bg-split tw-my-4"></div>

      <!-- 通讯信息 -->
      <ul class="tw-gap-y-4 tw-flex tw-flex-col">
        <li v-for="i in 5" :key="i" class="tw-flex tw-flex-row tw-items-center">
          <div class="tw-bg-amber-300 tw-rounded-full tw-w-7 tw-h-7"> </div>
          <div class="tw-ml-4 tw-flex tw-flex-col tw-text-xs">
            <span class="tw-text-invert tw-opacity-70">EMAIL</span>
            <span>dmc1253@163.com</span>
          </div>
        </li>
      </ul>

      <div class="tw-h-[1px] tw-bg-split tw-my-4"></div>

      <!-- 社交平台地址 -->
      <ul class="tw-flex tw-flex-row tw-gap-x-4">
        <li v-for="i in 3" :key="i" class="tw-bg-amber-300 tw-rounded-full tw-w-7 tw-h-7"></li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent, ref } from 'vue';

  export default defineComponent({
    name: 'SideBar',
    setup() {
      // 详情栏是否打开
      const iSopen = ref<Boolean>(false);

      /**
       * 切换打开关闭详情栏
       */
      const switchDetails = () => {
        iSopen.value = !iSopen.value;
      };

      return {
        switchDetails,
        iSopen
      };
    }
  });
</script>

<style>
  .fade-out-top {
    transition: 0.5s ease-in-out;
  }
</style>
