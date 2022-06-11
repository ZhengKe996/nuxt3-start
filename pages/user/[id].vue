<template>
  <div>{{ $route.params.id }}</div>
  <div>{{ route.params.id }}</div>
  <hr />
  <NuxtLayout name="custom"> Hello world! </NuxtLayout>
  <hr />
</template>

<script setup lang="ts">
// 加载模板
definePageMeta({
  layout: "custom",
});
const route = useRoute();
</script>

<style scoped></style>
