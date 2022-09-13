<template>
  <v-row>
    <section class="about-me" id="about">
      <v-img
        elevation="8"
        class="pa-10"
        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
        style="background-image:linear-gradient(to right, #333893 , rgb(224, 19, 115 , 0.7));"
      >
        <v-row justify="center" class="align-center">
          <v-col lg="6" xs="12">
            <v-card
              class="text-center pa-6 rounded-lg"
              color="#e1e0e0c9"
              elevation="6"
            >
              <v-card-subtitle class="green--text"
                >ABOUT MYSELF</v-card-subtitle
              >
              <h2 class="display-1 font-weight-regular">
                I am a developer with Laravel framework and a little with Vue
                Js. Since 2020 I've been doing freelance jobs and looking for a
                full-time or part-time position prefered(remotely), or
                freelance.
              </h2>
            </v-card>
          </v-col>
          <v-col lg="6" xs="12">
            <v-card class="pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
              <div class="py-1" v-for="(item, index) in items" :key="index">
                <label>{{ item.title }}</label>
                <v-progress-linear
                  :color="item.color"
                  height="10"
                  :value="item.value"
                ></v-progress-linear>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-img>
    </section>
  </v-row>
</template>

<script>
export default {
  name: "OverView",

  data: () => ({
    items: [
      { title: "PHP", value: 80, color: "red" },
      { title: "Laravel", value: 90, color: "light-blue" },
      { title: "Bootstrap", value: 80, color: "deep-orange" },
      { title: "Javascript", value: 75, color: "light-green" },
      { title: "Vuejs", value: 80, color: "blue" },
      { title: "Vuetify", value: 90, color: "black" },
      { title: "HTML5+CSS3", value: 90, color: "red" },
      { title: "Git", value: 75, color: "light-blue" },
      { title: "Mysql + Redis", value: 80, color: "light-green" },
    ],
  }),
};
</script>

<style></style>
