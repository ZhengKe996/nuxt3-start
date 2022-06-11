<template>
  <NuxtPage></NuxtPage>
  <NuxtLink to="/">index</NuxtLink>
  <hr />
  <NuxtLink to="/user/2">user/2</NuxtLink>
  <div>
    {{ data }}
    {{ count }}
    <hr />
    {{ foo }}
    <hr />
    <GoodsItem></GoodsItem>
  </div>
</template>

<script lang="ts" setup>
const { data } = await useAsyncData("count", () => $fetch("/api/count"));
const { data: count } = await useFetch("/api/count");

const foo = useFoo();

setTimeout(() => {
  foo.value = "Hello World";
}, 1000);
</script>
