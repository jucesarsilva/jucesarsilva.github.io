<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Julio Silva GitHub </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Páginas de Exemplos </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const linksList = [
  {
    title: 'HTML5 Game',
    caption: 'A game using eS6/html5/webpack/scss',
    icon: 'rocket_launch',
    link: 'https://jucesarsilva.github.io/html5-game/',
  },
  {
    title: 'React GitHub',
    caption: 'A website that consumes the GitHub API',
    icon: 'fingerprint',
    link: 'https://jucesarsilva.github.io/inception/',
  },
  {
    title: 'HTML5 Game Tile',
    caption: 'A Tile-based game',
    icon: 'sports_esports',
    link: 'https://jucesarsilva.github.io/html5-tiles-based-game/',
  },
  {
    title: 'PWA freelancer App',
    caption: 'A PWA private app',
    icon: 'app_shortcut',
    link: 'https://jucesarsilva.github.io/pauapixel-pwa.github.io/#/login',
  },
  {
    title: 'Shuffler algorithms',
    caption: 'A simples test algorithms',
    icon: 'functions',
    link: 'https://jucesarsilva.github.io/shuffler-algorithms/',
  },
  {
    title: 'Vuetify Masks pt-br',
    caption: 'Masks to use with Inputs Vuetify components',
    icon: 'tag',
    link: 'https://jucesarsilva.github.io/vuetify-masks-br/',
  },
  {
    title: 'Angular PWA Schedule',
    caption: 'Angular 8 study case',
    icon: 'schedule',
    link: 'https://jucesarsilva.github.io/point-control-angular',
  },
  {
    title: 'Alura Armazenando Web',
    caption: 'Curso: javascript na web armazenando dados no navegador',
    icon: 'school',
    link: 'https://jucesarsilva.github.io/alura/mochila-de-viagem/',
  },
  {
    title: 'Alura Typescript parte 1',
    caption: 'Curso: typescript parte 1: evoluindo seu javascript',
    icon: 'school',
    link: 'https://jucesarsilva.github.io/alura/typescript-curso-1/public/',
  },
  {
    title: 'Alura Typescript parte 2',
    caption: 'Curso: typescript parte 2: evoluindo seu javascript',
    icon: 'school',
    link: 'https://jucesarsilva.github.io/alura/typescript-curso-2/public/',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
