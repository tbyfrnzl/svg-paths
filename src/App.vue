<template>
  <v-app>
    <v-main>
      <v-container grid-list-md>
        <v-row>
          <Card v-for="path in paths" :key="path.pathTitle" v-bind:path="path" />
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

  data: () => ({
    paths: [
      {
        pathTitle: 'Test 1',
        path: 'M 123234',
        width: 6
      },
      {
        pathTitle: 'Test 2',
        path: '23432432',
        width: 6
      },
      {
        pathTitle: 'Test 3',
        path: '34543543',
        width: 4
      },
      {
        pathTitle: 'Test 4',
        path: '757456',
        width: 4
      },
      {
        pathTitle: 'Test 5',
        path: '23424i',
        width: 4
      },
      {
        pathTitle: 'Test 6',
        path: 'C 234252',
        width: 12
      }
    ]
  })
};
</script>
