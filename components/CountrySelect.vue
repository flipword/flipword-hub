<template>
  <div class="flex flex-row gap-2">
    <div class="flex flex-col pt-2">
      <div
        class="flex flex-col justify-center h-12 w-12 rounded-lg overflow-hidden"
      >
        <img :src="`/icons/flags/${flagPath}`" class="h-full w-full" />
      </div>
    </div>
    <select
      v-model="selectedLang"
      class="mr-5 mt-2 country-select"
      name="lang"
      @change="updateLang"
    >
      <option
        v-for="(lang, index) in langOptions"
        :key="index"
        :value="lang.id"
        :selected="selectedLang == lang.id"
      >
        {{ lang.label }}
      </option>
    </select>
  </div>
</template>

<script setup lang="ts">
import { computed, defineProps, defineEmits, ref } from "vue";
import { langOptions, flagPaths } from "~/plugins/i18n";

const emit = defineEmits(["changeLang"]);
const props = defineProps({
  currentLang: { default: "", type: String },
});
let selectedLang = ref(props.currentLang);
const flagPath = computed(() => flagPaths[selectedLang.value]);

const updateLang = () => {
  emit("changeLang", selectedLang.value);
};
</script>

<style scoped>
.country-select {
  background-color: transparent;
  outline: none;
  font-size: 20px;
  text-indent: -1px;
  border: none;
}
</style>
