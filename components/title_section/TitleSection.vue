<template>
  <div>
    <v-row v-if="stick">
          <div class="stick-vertical"></div>
    </v-row>
    <div class="text-center">
      <div class="about">
        <div class="container">
          <span class="text-center small_title bold" v-if="smallTitle">{{
            smallTitle
          }}</span>
          <h2 :class="'text-center heading-title ' + textColor" v-if="title">
            {{ title }}
          </h2>
          <h2 class="text-center heading-title" v-if="subTitle">
            {{ subTitle }}
          </h2>
        </div>
      </div>
      <p class="description ptb--10">
        {{ desc }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    smallTitle: { type: String, default: "" },
    title: { type: String, default: "" },
    subTitle: { type: String, default: "" },
    desc: {
      type: String,
      default: "",
    },
    stick: { type: Boolean, default: false},
    textColor: { type: String, default: "" },
  },
};
</script>
<style scoped>
.container {
  margin: 0 auto;
  width: 100%;
  text-align: center;
  padding: 5px;
  color: var(--color-primary);
}
.about:after {
  /* this is the border */
  content: "";
  display: block;
  width: 6em;
  max-width: 70%;
  border-bottom: 0.3em solid var(--color-secondary);
  margin: -1rem auto 0;
}
.container h2 {
  color: var(--color-primary);
}
.small_title {
  font-weight: bold;
  color: var(--color-secondary) !important;
}
.description {
  color: var(--color-primary) !important;
  justify-content: center;
}
.stick-vertical {
  margin: auto;
  height: 50px;
  width: 4px;
  background: var(--color-primary);
}
</style>
