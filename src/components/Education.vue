<template>
  <section class="educaion py-6">
    <v-container id="Education">
      <h4 class="display-2 text-center">Education</h4>
      <v-row class="py-8">
        <v-col cols="12" lg="6">
          <v-card class="pa-6 rounded-xl" elevation="5">
            <div class="d-flex align-center justify-space-between">
              <div class="">
                <h2>User Experience Designer</h2>
                <span>March 2020 - Present</span>
              </div>
              <a class="green--text"
                >at Dalian University <v-icon color="green">mdi-link</v-icon></a
              >
            </div>
            <v-card-text>
              Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec.
              Fusce eget urna ante. Donec massa velit, varius a accumsan ac,
              tempor iaculis massa. Sed placerat justo sed libero varius
              vulputate.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" lg="6">
          <v-card class="pa-6 rounded-xl" elevation="5">
            <div class="d-flex align-center justify-space-between">
              <div class="">
                <h2>UI Designer</h2>
                <span>March 2020 - Present</span>
              </div>
              <a class="green--text"
                >at School of California<v-icon color="green"
                  >mdi-link</v-icon
                ></a
              >
            </div>
            <v-card-text>
              Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec.
              Fusce eget urna ante. Donec massa velit, varius a accumsan ac,
              tempor iaculis massa. Sed placerat justo sed libero varius
              vulputate.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: "Education",

  data: () => ({}),
};
</script>

<style></style>
