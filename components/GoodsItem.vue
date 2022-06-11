<template>
  <div>{{ foo }}</div>
  <img :src="img" />
  <img src="/images/img.png" />
  <img :src="hed" />
</template>

<script setup lang="ts">
import img from "/images/img.png";
import hed from "/images/head.jpg";
const foo = useFoo();
</script>

<style scoped></style>
