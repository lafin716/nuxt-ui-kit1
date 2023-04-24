<script setup lang="ts">
import Navigation1 from '@/components/section/header/Header1.vue';

const title = ref("lacomm - Lafin의 커뮤니티");
useHead({
  meta: [{ content: title }],
  titleTemplate: (titleChunk) => {
    return titleChunk
      ? `${titleChunk} - Lafin의 커뮤니티`
      : "lacomm - Lafin의 커뮤니티";
  },
});
</script>

<template>
  <v-app dark>
    <Navigation1 />
    <v-main>
      <slot />  
    </v-main>
    <LcFooter/>
  </v-app>
</template>
