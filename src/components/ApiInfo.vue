<template>
  <div class="container mx-auto">
    <h1>{{ info.title }}</h1>
    <div>Base URL: [ {{ info.baseUrl }} ]</div>
    <div>{{ info.desc }}</div>
    <div>
      <a class="text-teal-700" :href="info.termsOfServiceUrl">
        Terms of service
      </a>
    </div>
    <div>
      <a class="hover:text-teal-700" :href="'mailto:' + info.contact.email">
        {{ info.contact.name }}'s email
      </a>
    </div>
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
          name: "Keyto",
          email: "keyto1995@outlook.com",
        },
      },
    };
  },
});
</script>
