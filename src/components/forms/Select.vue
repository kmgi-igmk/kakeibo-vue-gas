<template>
  <div class="col-auto">
    <div class="form-floating">
      <select id="inputSelect" class="form-select inputs" required></select>
      <label for="inputSelect" class="form-label">{{ label }}</label>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    label: String,
  },
});
</script>