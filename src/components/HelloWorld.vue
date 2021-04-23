<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>Using the bootstrap library in vue.js</h3>

    <!-- styling a button with bootstrap -->
    <button class="btn btn-primary">Click Me</button>

    <!-- styling a badge with bootstrap -->
    <h1>Example heading <span class="badge bg-secondary">New</span></h1>
    <button type="button" class="btn btn-primary">
      Notifications <span class="badge bg-secondary">4</span></button
    ><br />

    <!-- styling an alert with bootstrap-vue -->
    <b-alert show>Default Alert</b-alert> <br />
    <b-alert variant="success" show>Success Alert</b-alert> <br />

    <!-- adding a slide with vueperslides -->
    <vueper-slides>
      <vueper-slide v-for="i in 5" :key="i" :title="i.toString()" />
    </vueper-slides>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

export default {
  components: { VueperSlides, VueperSlide },
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: () => ({
    slides: [
      {
        title: "Slide #1",
        content: "Slide content.",
      },
    ],
  }),
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.vueperslide {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
}
</style>
