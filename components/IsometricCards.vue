<template>
  <div class="w-full h-full flex flex-row gap-32 ml-48">
    <div class="isometric flex flex-col gap-5 mt-48">
      <Card :word="wordList[props.lang][0]" />
    </div>
    <div class="isometric flex flex-col gap-5 -ml-48">
      <Card :word="wordList[props.lang][1]" />
      <Card :word="wordList[props.lang][2]" />
    </div>
    <div class="isometric flex flex-col gap-5 -mt-48 -ml-48">
      <Card :word="wordList[props.lang][3]" />
      <Card :word="wordList[props.lang][4]" />
      <Card :word="wordList[props.lang][5]" />
    </div>
    <div class="isometric flex flex-col gap-5 -mt-96 -ml-48">
      <Card :word="wordList[props.lang][6]" />
      <Card :word="wordList[props.lang][7]" />
      <Card :word="wordList[props.lang][8]" />
      <Card :word="wordList[props.lang][9]" />
    </div>
    <div class="isometric flex flex-col gap-5 -mt-110 -ml-12">
      <Card :word="wordList[props.lang][10]" />
      <Card :word="wordList[props.lang][11]" />
      <Card :word="wordList[props.lang][12]" />
      <Card :word="wordList[props.lang][12]" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";
import Card from "../components/Card.vue";
import { wordList } from "assets/data/words";

const props = defineProps({
  lang: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
.isometric {
  transform: rotateX(60deg) rotateY(0deg) rotateZ(-45deg);
}
</style>
