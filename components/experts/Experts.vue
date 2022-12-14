<template>
  <div class="bg-color">
    <v-row>
     <v-col
      cols="12">
      <div class="section-title white--text">
      <title-section :small-title="small_title" :text-color="text_color" :title="title"></title-section>
      </div>
    </v-col>
    <!-- Start Single Counterup  -->
    <v-col
      lg="3"
      md="3"
      sm="6"
      cols="12"
      class="im_single_counterup"
      v-for="(counter, i) in counterUpContent"
      :key="i"
    >
      <div class="im_counterup transparent">
        <div class="inner">
          <div class="icon" v-html="iconSvg(counter.icon)"></div>
          <h5 class="counter count white--text">
            <VisibilitySensor @change="onChange">
              <countTo
                :endVal="status ? counter.endVal : 0"
                :autoplay="countUp"
                :duration="3000"
              ></countTo>
            </VisibilitySensor>
          </h5>
          <p class="description white--text">
            {{ counter.desc }}
          </p>
        </div>
      </div>
    </v-col>
    <!-- Start Single Counterup  -->
  </v-row>
  </div>
</template>

<script>
  import VisibilitySensor from "vue-visibility-sensor";
  import countTo from "vue-count-to";
  import feather from "feather-icons";
  export default {
    components: {
      countTo,
      VisibilitySensor,
    },
    data() {
      return {
        small_title: 'Experts growth',
        title: 'Our Company Growth',
        text_color:'white--text',
        countUp: true,
        status: false,
        counterUpContent: [
          {
            icon: "heart",
            endVal: 199,
            desc: `Staticfied Customers`,
          },
          {
            icon: "clock",
            endVal: 575,
            desc: `Days Of Operation`,
          },
          {
            icon: "check-circle",
            endVal: 49,
            desc: `Complete Project`,
          },
          {
            icon: "award",
            endVal: 55,
            desc: `Win Awards`,
          },
        ],
      };
    },
    methods: {
      onChange(isVisible) {
        if (isVisible) {
          this.status = true;
        }
      },
      iconSvg(icon) {
        return feather.icons[icon].toSvg();
      },
    },
  };
</script>
<style scoped>
.bg-color {
  background-image: url('../../assets/images/19691.jpg');
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
