<template>
  <NuxtLink
    class="w-56 bg-white h-fit-content flex flex-row items-center pl-3 py-2 gap-5 rounded-lg border border-whiteShadow shadow-lg cursor-pointer"
    :to="storeLink"
    target="_blank"
  >
    <img
      :src="`/icons/stores/${props.storeImgPath}`"
      class="w-auto h-10"
      :alt="props.store"
    />
    <div class="flex flex-col">
      <span class="font-bold">{{ props.store }}</span>
      <span>{{ props.platform }}</span>
    </div>
  </NuxtLink>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps({
  store: {
    type: String,
    required: true,
  },
  platform: {
    type: String,
    required: true,
  },
  storeImgPath: {
    type: String,
    required: true,
  },
  storeLink: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
.h-fit-content {
  height: fit-content;
}
</style>
