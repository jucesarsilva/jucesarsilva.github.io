<template>
  <q-page class="column items-center justify-start q-px-lg q-py-lg">
    <q-parallax src="~assets/dogs.jpg" :height="200">
      <h5 class="text-white gandhi">"O amor é a força mais sutil do mundo."</h5>
    </q-parallax>
    <br />
    <br />
    <q-card flat bordered>
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://avatars.githubusercontent.com/u/22798551?v=4" />
          </q-avatar>
        </q-item-section>
        <q-item-section>
          <q-item-label>Julio Cesar da Silva Batista</q-item-label>
          <q-item-label caption>Bauru, São Paulo, Brasil</q-item-label>
        </q-item-section>
      </q-item>
      <q-separator />
      <q-card-section>
        <q-card-section>
          Estou atuando na área de tecnologia há 11 anos, sou graduado pela
          Fatec-Ourinhos em Desenvolvimento de Jogos Digitais, e pós graduado
          pela USC Bauru em Desenvolvimento de Sistemas Web Utilizando Java.
          Casado desde 2020, minha esposa se chama Érica e nosso filho Zaion
          (que nesse momento que escrevo está com 36 semanas no forninho da
          mamãe). Tenho 2 doguinhos, Ghost um macho pastor alemão de 6 anos e
          Gamora fêmea da mesma raça de 3 anos. Natural de Santa Cruz do Rio
          Pardo, mas residindo em uma casa térrea com bastante espaço no
          quintal, no bairro Mary Dota em Bauru. Como hobbies tenho tocar
          violão, jogar vídeo game, passear com os dogs.
        </q-card-section>
      </q-card-section>
      <q-separator />
      <q-card-actions>
        <a
          class="link"
          href="https://www.linkedin.com/in/julio-cesar-silva-dev/"
          target="_blank"
        >
          <q-icon class="text-dark" size="lg">
            <img src="~assets/linkedin.svg" />
          </q-icon>
        </a>
        <a
          class="link"
          href="https://www.facebook.com/julio.c3sar.silva/"
          target="_blank"
        >
          <q-icon class="text-dark" size="lg">
            <img src="~assets/facebook.svg" />
          </q-icon>
        </a>
        <a class="link" href="https://wa.me/+5514997965493" target="_blank">
          <q-icon class="text-dark" size="lg">
            <img src="~assets/whatsapp.svg" />
          </q-icon>
        </a>
        <a
          class="link"
          href="https://www.instagram.com/julioc_silva/"
          target="_blank"
        >
          <q-icon class="text-dark" size="lg">
            <img src="~assets/instagram.svg" />
          </q-icon>
        </a>
      </q-card-actions>
    </q-card>
    <br />
    <br />
    <q-card dark bordered class="bg-grey-9 my-card">
      <q-card-section>
        <div class="text-h6">Experiência Profissional</div>
      </q-card-section>
      <q-separator dark inset />
      <q-card-section>
        Tenho trabalhado como programador Frontend nos últimos anos, focado em
        JavaScript (ES5, ES6), HTML, CSS(Sass, Stylus), jQuery, AngularJS,
        Angular (TypeScript), Vue 2 (Vuetify, Quasar), React Web, Webpack,
        Grunt, Gulp, E2E, Unit tests. Nodejs + Express + Sequelize + MySql. Já
        desenvolvi alguns trabalhos como freelancer FullStack utilizando Java
        Spring MVC + JPA + JWT, Maven, MongoDB, MySQL, SQLServer. Sou pró-ativo,
        tenho paixão pelo desenvolvimento, encarando os projetos como uma parte
        importante da minha vida pessoal e profissional. Sempre disposto a
        aprender, ajudar os colegas, focando sempre nos prazos e na qualidade.
      </q-card-section>
    </q-card>
    <br />
    <br />
    <div class="flex-break row justify-start">
      <div class="q-pa-md" v-for="tech in techs" :key="tech.label">
        <q-card class="q-gutter-x-md">
          <q-card-section>
            <div class="text-h6">{{ tech.label }}</div>
          </q-card-section>
          <q-card-section>
            <q-rating
              v-model="tech.range"
              max="5"
              readonly
              size="28px"
              color="secondary"
              icon="star_border"
              icon-selected="star"
              icon-half="star_half"
            />
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>
<script lang="ts">
import { Tech } from 'components/models';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  setup() {
    const technologies = [
      {
        label: 'HTML 5',
        range: 5,
      },
      {
        label: 'JavaScript',
        range: 5,
      },
      {
        label: 'Css',
        range: 5,
      },
      {
        label: 'React',
        range: 4.5,
      },
      {
        label: 'TypeScript',
        range: 4,
      },
      {
        label: 'Sass',
        range: 4,
      },
      {
        label: 'Stylus',
        range: 3.5,
      },
      {
        label: 'AngularJs',
        range: 5,
      },
      {
        label: 'Angular 2+',
        range: 2.5,
      },
      {
        label: 'VueJs',
        range: 4,
      },
      {
        label: 'Java',
        range: 2.5,
      },
      {
        label: 'SQL',
        range: 2.5,
      },
      {
        label: 'MongoDB',
        range: 2,
      },
      {
        label: 'Spring MVC',
        range: 2,
      },
      {
        label: 'Spring JPA',
        range: 2,
      },
      {
        label: 'Maven',
        range: 3,
      },
      {
        label: 'JAVA JWT',
        range: 2,
      },
      {
        label: 'jQuery',
        range: 4.5,
      },
      {
        label: 'React Hooks',
        range: 4.5,
      },
      {
        label: 'React Class',
        range: 4.5,
      },
      {
        label: 'Jest',
        range: 4,
      },
      {
        label: 'Webpack',
        range: 4,
      },
      {
        label: 'Grunt',
        range: 4,
      },
      {
        label: 'Gulp',
        range: 4,
      },
      {
        label: 'Jasmine',
        range: 4,
      },
      {
        label: 'Karma',
        range: 4,
      },
      {
        label: 'Nodejs',
        range: 3,
      },
      {
        label: 'Express',
        range: 3,
      },
      {
        label: 'MySQL',
        range: 3,
      },
      {
        label: 'Workbench',
        range: 3,
      },
      {
        label: 'Scrum',
        range: 2.5,
      },
      {
        label: 'Kanban',
        range: 2.5,
      },
      {
        label: 'Sequelize',
        range: 2.5,
      },
      {
        label: 'SQLServer',
        range: 2.5,
      },
    ].sort((a, b) => (a.range > b.range ? -1 : 1));

    const techs = ref<Tech[]>(technologies);

    return { techs };
  },
});
</script>
