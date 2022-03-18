<template>
  <v-main>
    <v-container fluid>
      <div id="plot1" ref="plot1"></div>
      <v-btn @click="test">Test</v-btn>
    </v-container>
  </v-main>
</template>

<script>
import Plotly from "plotly.js-dist";

export default {
  name: "App",

  data: () => ({
    //
    count: 0,
    data: [{ x: [1, 2, 3, 4], y: [10, 15, 13, 17], type: "scatter" }],
    attr: { displayModeBar: true },
    layout: { title: "My graph :)" },
  }),
  methods: {
    test() {
      Plotly.newPlot("plot1", this.data);
    },
  },
  mounted() {
    this.test();
  },
};
</script>
