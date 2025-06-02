<template>
  <div>
    <NuxtLinkLocale v-if="logo.light && logo.dark" :to="localePath('/')" class="flex">
      <span v-if="showTitle && title" class="ml-3 self-center font-bold">
        Výchova ke zdraví
      </span>
    </NuxtLinkLocale>
  </div>
</template>

<script setup lang="ts">
const { logo, title, showTitle } = useConfig().value.header;
const { localePath } = useI18nDocs();
</script>
