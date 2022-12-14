<template>
  <div class="pt-16 pb-16 back-ground">
    <v-container>
      <v-row justify="center" class="pt-16 pb-16">
        <v-col cols="12" md="6" sm="12">
          <h1 class="color">{{$t("A customized learning experiences")}}</h1>
        </v-col>
        <v-divider vertical color="#fff"></v-divider>
        <v-col cols="12" md="6" sm="12">
          <p class="mt-15 color">
            {{
              $t(
                "Deliver the right learning experience to the right people in the right format.with learnKhana business,you've got option for everyone."
              )
            }}
          </p>
          <!-- <v-row justify="start">
          <v-btn class="ms-7 padding" color="secondary" rounded
            ><span>Learn more</span
            ><v-icon>{{ `mdi-arrow-${$vuetify.rtl ? "left" : "right"}` }}</v-icon></v-btn
          >
          <v-btn class="ms-7 padding" color="secondary" rounded
            ><v-icon>mdi-play-circle </v-icon>
            <span>Learn more</span></v-btn
          >
        </v-row> -->
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style lang="scss">
.back-ground {
  background: linear-gradient(to bottom, #fff 0, var(--color-primary) 100%);
}
.color {
  color: var(--color-primary) !important;
  font-size: 64px;
}
p {
  color: var(--color-primary) !important;
  font-size: 20px !important;
  line-height: 45px !important;
}
@media (width<767px) {
  .color {
    font-size: 32px;
    text-align: center;
  }
}
@media (width<375px) {
  .padding {
    padding: 0px 0px 0px 0px !important;
  }
}
</style>
