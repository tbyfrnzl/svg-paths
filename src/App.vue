<template>
  <v-app>
    <v-main>
      <v-container grid-list-md>
        <v-row>
          <Card v-for="(path, index) in paths" :key="path.pathTitle" v-bind:path="path" v-bind:card-index="getCardIndex(index)" />
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Card from './components/Card.vue';
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    Card
  },
  methods: {
    getCardIndex(index) {
      return `card-${index}`
    }
  },
  data: () => ({
    paths: [
      {
        pathTitle: 'Horizontal line',
        path: 'M30,150 L309,150',
        width: 4,
        className: 'horizontal-line'
      },
      {
        pathTitle: 'Vertical line',
        path: 'M170,50 L170,250',
        width: 4,
        className: 'vertical-line'
      },
      {
        pathTitle: 'Crossing lines (horizontal + vertical)',
        path: 'M170,50 L170,250 M50,150 L289,150',
        width: 4,
        className: 'line-cross'
      },
      {
        pathTitle: 'Cross',
        path: 'M150,75 h50 v50 h50 v50 h-50 v50 h-50 v-50 h-50 v-50 h50 v-50 z',
        width: 6,
        className: 'cross'
      },
      {
        pathTitle: 'Lying Long Cross',
        path: 'M150,75 h50 v50 h200 v50 h-200 v50 h-50 v-50 h-50 v-50 h50 v-50 z',
        width: 6,
        className: 'lying-cross'
      },
      {
        pathTitle: 'Mountains',
        path: 'M0,300 L50,100 L100,200 L120,180',
        width: 12,
        className: 'mountains'
      }
    ]
  })
};
</script>
