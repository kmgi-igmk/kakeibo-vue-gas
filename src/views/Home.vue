<template>
  <div class="home">
    <Register title="ためため家計簿" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Register from "@/components/Register.vue"; // @ is an alias to /src

export default defineComponent({
  name: "Home",
  components: {
    Register,
  },
});
</script>
