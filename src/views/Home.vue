<template>
  <div class="home container">
    <Alert />
    <Header />
    <Register />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
// @ is an alias to /src
import Alert from "@/components/Alert.vue";
import Header from "@/components/Header.vue";
import Register from "@/components/Register.vue";

export default defineComponent({
  name: "Home",
  components: {
    Alert,
    Header,
    Register,
  },
});
</script>
