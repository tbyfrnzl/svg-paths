<template>
  <v-col :cols="path.width">
    <v-card tile :id="cardIndex">
      <v-card-title>{{ path.pathTitle }}</v-card-title>
      <v-card-text>
        <svg :viewBox="viewBox" ref="svg" :class="path.className">
          <path :d="path.path" stroke-width="2"></path>
        </svg>
        <small>Path: {{ path.path }}</small>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: 'Card',
  props: ['path', 'cardIndex'],
  data: function () {
    return {
      viewBox: ''
    };
  },
  mounted: function () {
    const svg = this.$refs.svg;
    const svgData = svg.getBoundingClientRect();

    console.log(svgData)

    this.viewBox = `0 0 ${svgData.width} 300`;
  }
};
</script>

<style scoped>
svg {
  width: 100%;
  height: 300px;
  stroke: black;
  fill: none;
  background-color: whitesmoke;
}
.lying-cross {
    fill: pink;
    stroke: pink;
}
</style>
