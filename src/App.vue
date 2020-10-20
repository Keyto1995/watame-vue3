<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">{{ msg }}</router-link>
  </div>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  data() {
    return {
      msg: "POI",
    };
  },
});
</script>

<style lang="scss"></style>
