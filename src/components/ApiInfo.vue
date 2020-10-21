<template>
  <div class="container mx-auto">
    <h1>{{ info.title }}</h1>
    <div>Base URL: [ {{ info.baseUrl }} ]</div>
    <div>{{ info.desc }}</div>
    <a class="text-teal-700" :href="info.termsOfServiceUrl">Terms of service</a>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "ApiInfo",
  data() {
    return {
      info: {
        title: "演示项目API",
        desc: "watame 的演示项目",
        baseUrl: "127.0.0.1:8080/",
        version: "1.0.0",
        termsOfServiceUrl: "https://blog.keyto.top",
        contact: {
          name: "联系人",
          email: "邮箱地址",
        },
      },
    };
  },
});
</script>
