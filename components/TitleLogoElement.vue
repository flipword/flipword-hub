<template>
  <div class="md:h-3/5 h-2/5 md:3/4 w-4/5 relative">
    <div
      class="w-full top-0 -right-2 -bottom-1 bg-whiteShadow md:rounded-b-5xl rounded-b-3xl absolute shadow-md"
    ></div>
    <div
      class="h-full w-full bg-white md:rounded-b-5xl rounded-b-3xl relative flex justify-center items-center"
    >
      <div class="h-5/6 w-5/6 bg-primary md:rounded-b-5xl rounded-b-3xl">
        <div
          class="w-full h-full pb-20 flex flex-col justify-center items-center"
        >
          <div class="w-full flex flex-row justify-center">
            <img src="~/assets/icons/logo.svg" class="h-full w-1/4" />
            <div class="flex flex-col justify-center">
              <span
                class="font-sans 2xl:text-8xl xl:text-7xl lg:text-6xl xs:text-6xl text-4xl text-black font-bold"
                >FlipWord</span
              >
            </div>
          </div>
          <div class="w-full flex justify-center">
            <span
              class="font-sans 2xl:text-4xl xl:text-3xl lg:text-2xl text-xl text-black text-center"
              >{{ $t("subtitle") }}</span
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useNuxtApp } from "#app";

const {
  $i18n: { $t },
} = useNuxtApp();
</script>
