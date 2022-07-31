<template>
  <ul
    class="hover:tw-bg-red tw-flex tw-flex-row tw-bg-split tw-rounded-t-xl tw-justify-center tw-opacity-[97%] tw-fixed tw-bottom-0 tw-left-0 tw-right-0"
  >
    <li v-for="(item, index) in buttonGroup" :key="index">
      <button
        class="tw-py-5 tw-px-1 tw-text-xs"
        :class="focusTab === item ? 'tw-text-active' : 'tw-text-main'"
        @click="switchPage(item)"
        >{{ item }}</button
      >
    </li>
  </ul>
</template>
<script lang="ts">
  import { defineComponent, ref } from 'vue';

  export default defineComponent({
    name: 'NavBar',
    setup() {
      const buttonGroup: string[] = ['About', 'Resume', 'Portfolio', 'Blog', 'Contact'];

      let focusTab = ref<string>('About');

      const switchPage = (item: string) => {
        focusTab.value = item;
        console.log('🚀liu ~ file: NavBar.vue ~ line 27 ~ switchPage ~ focusTab', focusTab.value);
      };
      return {
        buttonGroup,
        switchPage,
        focusTab
      };
    }
  });
</script>
