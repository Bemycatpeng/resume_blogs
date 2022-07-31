<template>
  <div class="tw-bg-card tw-p-4 tw-rounded-2xl tw-text-white">
    <!-- 关于我 -->
    <h1 class="tw-text-2xl">关于我</h1>
    <div class="tw-h-[3px] tw-bg-yellow-400 tw-rounded-md tw-w-7 tw-mt-1 tw-mb-2"></div>
    <div class="tw-text-muted tw-text-sm">
      我是来自中国上海的一名前端开发工程师,从事web前端开发和多端app应用开发工作。目前在上海工作，拥有丰富的经验，我喜欢将复杂的问题转化为简单、美观和直观的交互体验。
      我的工作方向是前端开发，我的目标是在职位接收时能够提供良好的工作环境和技术支持，并且能够为我的团队提供更好的开发环境。
    </div>

    <!-- 我是做什么的 -->
    <h2 class="tw-text-lg tw-mt-3">我是做什么的</h2>
    <div
      v-for="i in 4"
      :key="i"
      class="tw-mt-3 tw-flex tw-flex-col tw-items-center tw-border tw-rounded-xl tw-p-4"
    >
      <div class="tw-bg-amber-300 tw-rounded-full tw-w-7 tw-h-7 tw-mb-2"> </div>
      <div class="tw-mb-2">Web Design</div>
      <div class="tw-text-center"
        >The most modern and high-quality design made at aprofessional level.</div
      >
    </div>

    <!-- 感言 -->
    <h2 class="tw-text-lg tw-my-7">感言</h2>
    <ul
      class="tw-gap-x-6 tw-flex tw-flex-row tw-overflow-y-auto tw-scroll-smooth tw-pt-10 tw-pb-6 tw-snap-mandatory tw-snap-x has-scrollbar"
    >
      <li
        v-for="i in 3"
        :key="i"
        class="tw-border tw-border-white tw-pt-14 tw-pb-4 tw-px-4 tw-rounded-xl tw-relative tw-min-w-full tw-snap-center"
      >
        <div class="tw-w-20 tw-rounded-xl tw-bg-split tw-absolute tw--top-9">
          <img src="images/my-avatar.png" />
        </div>
        <h3 class="tw-mb-3 tw-text-base">Daniel lewis</h3>
        <div class="tw-text-sm tw-line-clamp-4">
          Richard was hired to create a corporate identity. We were very pleased with the work done.
          She has a lot of experience and is very concerned about the needs of client. Lorem ipsum
          dolor sit amet, ullamcous cididt consectetur adipiscing elit, seds do et eiusmod tempor
          incididunt ut laborels dolore magnarels alia.
        </div>
      </li>
    </ul>

    <!-- 客户 -->
    <h2 class="tw-text-lg tw-my-7">客户</h2>
    <ul
      class="tw-pb-6 tw-flex tw-flex-row tw-gap-x-3 tw-overflow-x-auto tw-snap-x tw-snap-mandatory has-scrollbar"
    >
      <li v-for="i in 6" :key="i" class="tw-snap-start tw-min-w-[50%]">
        <img :src="`images/logo-${i}-color.png`" alt="" />
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'MainContent',
    setup() {}
  });
</script>

<style scoped>
  .has-scrollbar::-webkit-scrollbar {
    width: 5px;
    height: 5px;
  }

  .has-scrollbar::-webkit-scrollbar-track {
    background: hsl(240, 1%, 17%);
    border-radius: 5px;
  }

  .has-scrollbar::-webkit-scrollbar-thumb {
    background: hsl(45, 100%, 72%);
    border-radius: 5px;
  }

  .has-scrollbar::-webkit-scrollbar-button {
    width: 10px;
  }
</style>
