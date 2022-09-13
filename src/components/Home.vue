<template>
    <section class="intro-section my-5" id="home">
        <v-row class="align-center px-10" style="height: 22%">
          <v-col lg="6" xs="12"  class="pa-6 font-weight-bold py-16">
            <h2 class="display-3">
              As a Developer with <b>Vue js</b> and <b>Laravel</b>
            </h2>
            <v-subheader>Hi, I am Ossama, this is my portfolio.</v-subheader>
            <br />
            <br />
            <v-btn
              large
              elevation="9"
              color="green"
              class="rounded-xl white--text mx-0 mt-10 px-10 py-5 my_button"
              @click="$vuetify.goTo('#Contact', options)"
              >Hire Me</v-btn
            >
            <v-btn
              large
              elevation="9"
              color="pink"
              class="white--text mt-10 ml-4 ml-sm-0 px-10 py-5 rounded-xl my_button"
              @click="$vuetify.goTo('#Contact', options)"
              >Contact
            </v-btn>
            <v-row class="mt-16 icons">
              <v-btn
                href="https://www.facebook.com/ossama.abdabd"
                class="px-4 ma-3 my_icon"
                color="primary"
                target="_blank"
                fab
                small
              >
                <v-icon size="35">mdi-facebook</v-icon>
              </v-btn>
              <v-btn
                href="https://web.whatsapp.com/"
                class="px-4 ma-3 white--text my_icon"
                color="#01ff56"
                target="_blank"
                fab
                small
              >
                <v-icon size="35">mdi-whatsapp</v-icon>
              </v-btn>
              <v-btn
                href="https://stackoverflow.com/users/15622823/ossama-abd"
                class="px-4 ma-3 white--text my_icon"
                color="#ffc113"
                target="_blank"
                fab
                small
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="25"
                  height="25"
                  fill="currentColor"
                  class="bi bi-stack-overflow"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M12.412 14.572V10.29h1.428V16H1v-5.71h1.428v4.282h9.984z"
                  />
                  <path
                    d="M3.857 13.145h7.137v-1.428H3.857v1.428zM10.254 0 9.108.852l4.26 5.727 1.146-.852L10.254 0zm-3.54 3.377 5.484 4.567.913-1.097L7.627 2.28l-.914 1.097zM4.922 6.55l6.47 3.013.603-1.294-6.47-3.013-.603 1.294zm-.925 3.344 6.985 1.469.294-1.398-6.985-1.468-.294 1.397z"
                  />
                </svg>
              </v-btn>

              <v-btn
                href="https://www.linkedin.com/in/ossama-abd-rabouh-1535a7210/"
                class="px-4 ma-3 my_icon"
                color="info"
                target="_blank"
                fab
                small
              >
                <v-icon size="35">mdi-linkedin</v-icon>
              </v-btn>
              <v-btn class="px-4 ma-3 my_icon" color="primary" 
              href="https://t.me/OssamaAbdBot"
              target="_blank"
              fab small>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="30"
                  height="30"
                  fill="currentColor"
                  class="bi bi-telegram"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8.287 5.906c-.778.324-2.334.994-4.666 2.01-.378.15-.577.298-.595.442-.03.243.275.339.69.47l.175.055c.408.133.958.288 1.243.294.26.006.549-.1.868-.32 2.179-1.471 3.304-2.214 3.374-2.23.05-.012.12-.026.166.016.047.041.042.12.037.141-.03.129-1.227 1.241-1.846 1.817-.193.18-.33.307-.358.336a8.154 8.154 0 0 1-.188.186c-.38.366-.664.64.015 1.088.327.216.589.393.85.571.284.194.568.387.936.629.093.06.183.125.27.187.331.236.63.448.997.414.214-.02.435-.22.547-.82.265-1.417.786-4.486.906-5.751a1.426 1.426 0 0 0-.013-.315.337.337 0 0 0-.114-.217.526.526 0 0 0-.31-.093c-.3.005-.763.166-2.984 1.09z"
                  />
                </svg>
              </v-btn>
            </v-row>
          </v-col>
          <v-col lg="6" xs="12">
            
            <v-img
              class="mx-4 my_image"
              style="border-radius:50% ;"
              src="../assets/my image.jpg"
            ></v-img>
          </v-col>
        </v-row>
      </section>
</template>

<script>
export default {
  name: "Home",

  data: () => ({}),
};
</script>
