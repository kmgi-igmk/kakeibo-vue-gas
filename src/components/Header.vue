<template>
  <header>
    <div
      class="
        row
        p-1
        pb-md-3
        mx-auto
        justify-content-md-center
        align-items-center
        row-cols-auto
      "
    >
      <div class="col-md-auto px-0">
        <select class="form-select" v-model="currentYear">
          <option v-for="(year, index) in getYears" :key="index" :value="year">
            {{ year }}年
          </option>
        </select>
      </div>
      <h1 class="mb-0">{{ title }}</h1>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "Header",
  setup() {
    const title = ref("ためため家計簿");
    const currentYear = new Date().getFullYear();
    const getYears = Array.from(Array(3), (_, i) => currentYear - 1 + i);
    return {
      title,
      currentYear,
      getYears,
    };
  },
});
</script>

<style scoped>
</style>
