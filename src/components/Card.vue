<template>
  <v-col :cols="path.width">
    <v-card tile>
        <v-card-title>{{path.pathTitle}}</v-card-title>
        <v-card-text>
            <svg></svg>
            <small>{{path.path}}</small>
        </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: 'Card',
  props: ['path']
};
</script>

<style scoped>
svg {
    width: 100%;
    background-color: blue;
}
</style>
