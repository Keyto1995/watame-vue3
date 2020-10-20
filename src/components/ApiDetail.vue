<template>
  <div class="my-2 border" :class="colorClass">
    <div class="flex items-center" @click="visible = !visible">
      <div class="w-20 m-2 py-1 text-lg text-center">
        {{ apiDetail.method }}
      </div>
      <div class="px-1">{{ apiDetail.url }}</div>
      <div class="px-2 text-gray-800">{{ apiDetail.name }}</div>
    </div>
    <div v-show="visible">poi</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "ApiDetail",
  props: {
    apiDetail: Object,
  },
  data() {
    return {
      visible: true,
    };
  },
  computed: {
    colorClass() {
      switch (this.apiDetail.method) {
        case "GET":
          return "green";
        case "POST":
          return "yellow";
        case "PUT":
          return "blue";
        case "DELETE":
          return "red";

        default:
          return "";
      }
    },
  },
});
</script>

<style lang="scss" scoped>
.green {
  @apply border-green-500;
  > div:first-child {
    @apply bg-green-200;
    > div:first-child {
      @apply bg-green-400;
    }
  }
  > div:nth-child(2) {
    @apply bg-green-100;
  }
}

.yellow {
  @apply border-yellow-500;
  > div:first-child {
    @apply bg-yellow-200;
    > div:first-child {
      @apply bg-yellow-400;
    }
  }
  > div:nth-child(2) {
    @apply bg-yellow-100;
  }
}

.blue {
  @apply border-blue-500;
  > div:first-child {
    @apply bg-blue-200;
    > div:first-child {
      @apply bg-blue-400;
    }
  }
  > div:nth-child(2) {
    @apply bg-blue-100;
  }
}

.red {
  @apply border-red-500;
  > div:first-child {
    @apply bg-red-200;
    > div:first-child {
      @apply bg-red-400;
    }
  }
  > div:nth-child(2) {
    @apply bg-red-100;
  }
}
</style>
