<template>
  <i :data-feather="icon" class="center"></i>
</template>

<script>
import feather from "feather-icons";
export default {
  props: ["icon"],
  mounted() {
    feather.replace();
  }
};
</script>

<style>
.center {
  margin: auto;
}
</style>