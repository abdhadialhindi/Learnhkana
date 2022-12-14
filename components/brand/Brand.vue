<template>
  <div>
  <v-container>
    <v-row justify="center">
      <v-col :cols="`${
          $vuetify.breakpoint.name == 'xs' ||
          $vuetify.breakpoint.name == 'sm'

            ? '11'
            : '12'
        }`">
        <v-row justify="center" align="center">
          <v-col cols="12" sm="12" md="12" xs="12" >
          <v-row justify="center">

          <v-card class="border-raduis py-5 "  height="140"  elevation="16">

              <v-slide-group class="pa-2 ">
                <template v-slot:next >
                  <v-icon
                    color="primary"
                    :class="$vuetify.rtl ? 'icon-one' : 'icon-tow'"
                    >{{ `mdi-arrow-${$vuetify.rtl ? "left" : "right"}` }}</v-icon
                  >
                </template>
                <template v-slot:prev>
                  <v-icon
                    color="primary"
                    :class="$vuetify.rtl ? 'icon-tow' : 'icon-one'"
                    >{{ `mdi-arrow-${$vuetify.rtl ? "right" : "left"}` }}</v-icon
                  >
                </template>
                <v-slide-item v-for="(item, index) in items" :key="index">
                <v-row justify="center">
                <v-card class="ms-8  " elevation="0" width="160">
                <v-row justify="center">

                 <v-img :src="item.src"   class="ms-5 m-2" height="80" contain  />
                </v-row>
                </v-card>
              </v-row>

                </v-slide-item>
              </v-slide-group>
            </v-card>
          </v-row>

          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</div>
</template>
<script>
export default {
  data: () => ({
    model: null,
    items: [
      {
        src: require("@/assets/images/brand/brand-01.png")
      },
      {
        src: require("@/assets/images/brand/brand-02.png"),
      },
      {
        src: require("@/assets/images/brand/brand-03.png"),
      },
      {
        src: require("@/assets/images/brand/brand-04.png"),
      },
      {
        src: require("@/assets/images/brand/brand-05.png"),
      },
      {
        src: require("@/assets/images/brand/brand-06.png"),
      },
      {
        src: require("@/assets/images/brand/brand-07.png"),
      },
      {
        src: require("@/assets/images/brand/brand-08.png"),
      },
      {
        src: require("@/assets/images/brand/brand-09.png"),
      },
    ],
  }),
};
</script>
<style lang="scss" scoped>
.icon-one {
  border: 2px solid var(--color-primary);
  border-radius: 50%;
  width: 25px;
  height: 25px;
  pointer-events: auto !important;

}
.icon-tow {
  border: 2px solid var(--color-primary);
  border-radius: 50%;
  width: 25px;
  height: 25px;
  pointer-events: auto !important;

}
.icon-one:hover{
  background-color: var(--color-primary);
  color: #fff !important;
}
.icon-tow:hover{
  background-color: var(--color-primary);
  color: #fff !important;
}
.border-raduis{
  border-radius: 18px;
  position: absolute ;
  bottom: 0%;
  transform: translatey(50%);
}
</style>
