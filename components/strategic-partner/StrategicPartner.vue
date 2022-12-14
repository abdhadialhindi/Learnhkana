<template>
  <div class="bg-color pt--50 pb--80">
    <v-row>
     <v-col
      cols="12">
      <div class="section-title pb--50">
        <h2 class='text-center heading-title'>
            <span class="white--text">{{ titleWithWhite }}</span> <span class="title-color">{{ titleWithYellow }}</span>
          </h2>
          <p class="text-center white--text" style="font-size: 30px"
          >
            {{ subTitle }}
        </p>
      </div>
    </v-col>
    <v-col align="center">
      <v-btn class="my-2" color="secondary" x-large rounded to='/contact'>{{
          $t("Contact with us")
        }}</v-btn>
    </v-col>
    <!-- Start Single Counterup  -->

    <!-- Start Single Counterup  -->
  </v-row>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        titleWithWhite: this.$t("We're your"),
        titleWithYellow: this.$t('strategic partner.'),
        subTitle:  this.$t("Let's move skills forward to gether!"),
      };
    },
  };
</script>
<style scoped>
.bg-color {
  background-image: url('../../assets/images/pexels-gradienta.jpg');
  background-repeat: no-repeat;
  background-size: contain cover;
  opacity: 0 .7;
}
.title-color {
  color: var(--color-secondary);
}
</style>
