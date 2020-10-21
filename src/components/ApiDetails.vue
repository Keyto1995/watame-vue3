<template>
  <div class="container mx-auto">
    <api-detail
      v-for="api in apis"
      :key="api.order"
      :apiDetail="api"
    ></api-detail>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ApiDetail from "./ApiDetail.vue";
export default defineComponent({
  name: "ApiDetails",
  components: {
    ApiDetail,
  },
  data() {
    return {
      apis: [
        {
          name: "列出所有商品",
          desc: "list goods",
          order: 0,
          method: "GET",
          url: "/goods",
        },
        {
          name: "新增商品",
          desc: "",
          order: 1,
          method: "POST",
          url: "/goods",
          body_mode: "json",
          body: {
            name: { name: "商品名称" },
            price: { name: "商品价格" },
          },
        },
        {
          name: "获取指定商品",
          desc: "getByID",
          order: 2,
          method: "GET",
          url: "/goods/{id}",
          query: {
            id: { name: "商品ID" },
          },
        },
        {
          name: "更新商品",
          desc: "",
          order: 3,
          method: "PUT",
          url: "/goods/{id}",
          body_mode: "json",
          body: {
            name: { name: "商品名称" },
            price: { name: "商品价格" },
          },
        },
        {
          name: "删除商品",
          desc: "",
          order: 4,
          method: "DELETE",
          url: "/goods/{id}",
          query: {
            id: { name: "商品ID" },
          },
        },
      ],
    };
  },
});
</script>
