<template>
  <div class="pt--50">
    <v-container cl>
      <v-row class="row--35 ptb--50" align="center">
      <v-col lg="7" md="7" cols="12">
        <div class="about-inner inner">
          <div class="section-title">
            <!-- <span class="subtitle">My About Details</span> -->
            <h1 class="heading-title title-color" >
              About Us <span class="dot-color">.</span>
              <div class=" ptb--15">
                <div class="hr-color"></div>
              </div>


            </h1>

            <p class="description mt_dec--20">
              There are many variations of passages of Lorem Ipsum available, but
              the majority have suffered in some form, by injected humour.
            </p>
          </div>
          <!-- End .section-title -->
          <div class="tab-wrapper mt--30">
            <v-row>
              <Tab />
            </v-row>
          </div>
          <v-col>
            <v-btn class="my-2" color="primary" x-large rounded to='/contact'>{{
                $t("View All Work")
              }}</v-btn>
          </v-col>
        </div>
      </v-col>
      <v-col lg="5" md="5" cols="12">
        <div class="thumbnail">
          <img
                slot="thum-img"
                class="w-100"
                src="../../assets/images/about/about-7.jpg"
                alt="About Images"
              />
        </div>
      </v-col>
    </v-row>
    </v-container>
  </div>
</template>

<script>
  import Tab from "../../components/tabs/Tab";
  export default {
    components: { Tab },
    data() {
      return {
        title: "About Us"
      };
    },
  };
</script>
<style>
.title-color {
  color: var(--color-primary)
}
.hr-color {
  background-color: var(--color-secondary) !important;
  width: 21%;
  height: 5px;
}
.dot-color {
  color: var(--color-secondary) !important;
  font-size: 120%;
}
</style>
