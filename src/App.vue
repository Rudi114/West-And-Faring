<template lang="pug">
  v-app
    TitlePage
    StickyNotePage
    WorkPage
    AboutPage
    ContactPage
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import TitlePage from '@/components/TitlePage.vue';
import StickyNotePage from '@/components/StickyNotePage.vue';
import WorkPage from '@/components/WorkPage.vue';
import AboutPage from '@/components/AboutPage.vue';
import ContactPage from '@/components/ContactPage.vue';

export default Vue.extend({
  name: 'App',

  components: {
    TitlePage,
    StickyNotePage,
    WorkPage,
    AboutPage,
    ContactPage,
  },
});
</script>

<style lang="scss" scoped>
  .template{
    scroll-behavior: smooth;
    width: 100vw;
    overflow-y: scroll;
    overflow-x: hidden;
    scroll-snap-type: y mandatory;
  }
</style>
