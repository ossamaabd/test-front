<template>
  <section class="experiance pb-6">
    <v-img class="pa-10" src="../assets/experiance.jpg" lazy>
      <v-container>
        <h4 class="display-2 text-center">Experience</h4>

        <v-timeline>
          <v-timeline-item
            v-for="(exper, index) in experience"
            :key="index"
            :color="index % 2 === 0 ? 'green' : 'blue'"
          >
            <v-card class="rounded-xl">
              <v-card-title :color="index % 2 === 0 ? 'pink' : 'green'">
                {{ exper.title }}
              </v-card-title>
              <v-card-text>
                <b>{{ exper.date }}</b
                ><br />
                <b>@{{ exper.institute }}</b
                ><br />
                {{ exper.decription }}
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-container>
    </v-img>
  </section>
</template>

<script>
export default {
  name: "Experiance",
  props: ["items"],
  components: {},
  data: () => ({
    drawer: null,

    experience: [
      {
        title: "Web Developer at Haram Internal Transfers",
        date: "November 2021 - Present",
        institute: "Web Developer",
        decription:
          "some project and integration Apis with other companies supported with Laravel and Vue js framewrok with MVC design pattern, clean code, relationships ,ORM, Cron Jops, authentication and middleware ...etc",
      },
      {
        title: "Backend Developer",
        date: "December 2020 - April 2021",
        institute: "Freelancer",
        decription:
          "I worked with flutter team as backend with laravel to present drug store application related with pharmacies",
      },
      {
        title: "Backend Developer",
        date: "March 2021 - August 2021",
        institute: "Freelancer",
        decription:
          "I worked with front web developer team as backend with laravel to present reservation system hotel",
      },
    ],
  }),
};
</script>
