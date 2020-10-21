<template>
  <header class="container mx-auto bg-white">
    <div class="flex items-center">
      <img height="50" width="50" alt="Vue logo" src="./assets/logo.png" />
      <span class="text-2xl">watame</span>
    </div>
  </header>
  <api-info />
  <api-details />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ApiInfo from "./components/ApiInfo.vue";
import ApiDetails from "./components/ApiDetails.vue";
export default defineComponent({
  name: "App",
  components: {
    ApiInfo,
    ApiDetails,
  },
  data() {
    return {};
  },
});
</script>
