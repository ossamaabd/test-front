<template>
  <section class="contact-us pt-10 pb-0" id="Contact">
    <v-img
      class="pt-10"
      gradient="to bottom, rgb(166 199 156), rgb(227 227 227 / 86%)"
      src="https://img.freepik.com/free-photo/contact-us_36325-2135.jpg?size=626&ext=jpg"
    >
      <v-container>
        <h4 class="display-1 text-center mb-5">
          This page is build by Vue js with Vuetify.
        </h4>
        <v-divider />
        <br />
        <v-row>
          <v-col cols="12" lg="6">
            <v-card-title>DROP A LINE</v-card-title>
            <v-form class="ma-4" ref="form">
              <v-text-field label="Your Name" v-model="name" :rules="rules" />
              <v-text-field label="Email" v-model="email" :rules="email_rule" />
              <v-text-field label="Subject" v-model="subject" :rules="rules" />
              <v-textarea label="Message" v-model="message" :rules="rules" />
              <v-btn
                @click="SendMessage"
                large
                color="green"
                class="rounded-xl white--text my_button"
                >Send Message</v-btn
              >
            </v-form>
          </v-col>
          <v-col cols="12" lg="3" offset="2">
            <v-card-title>CONTACT ME</v-card-title>
            <v-card-text>
              Damascus, <br />
              +963-965337936, <br />
              ossama.abd.sy@gmail.com <br />
            </v-card-text>
            <v-card-actions>
              <v-btn
                @click="DownloadResume"
                href="../files/Ossama Abd Rabouh.pdf"
                download
                large
                elevation="5"
                color="pink"
                class="white--text mt-10 px-10 py-5 rounded-xl my_button"
                >Download Resume
                <v-icon>mdi-download</v-icon>
              </v-btn>
            </v-card-actions>
          </v-col>
        </v-row>
      </v-container>
      <v-footer class="mt-4 mb-0">
        <v-col class="text-center" cols="12">
          <strong
            >Copyright ©{{ new Date().getFullYear() }}
            This is made by
            <a href="" class="green--text">Ossama Abd Rabouh</a>
          </strong>
        </v-col>
      </v-footer>
    </v-img>
  </section>
</template>

<script>
import axios from "axios";

export default {
  name: "Contact",

  data: () => ({
    rules: [(value) => !!value || "Required."],
    email_rule: [
      (value) => !!value || "Required.",
      (value) =>
        !value ||
        /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(value) ||
        "Email must be valid",
    ],
    name: "",
    email: "",
    subject: "",
    message: "",
    res: "",
  }),

  methods: {
    SendMessage() {
      if (this.$refs.form.validate()) {
        axios
          .post("https://ossamabottelegram.herokuapp.com/api/SendMessage", {
            name: this.name,
            email: this.email,
            subject: this.subject,
            message: this.message,
          })
          .then((response) => {
            if (response.data.code == 200) {
              this.$swal.fire({
                position: "top-end",
                icon: "success",
                title: response.data.message,
                showConfirmButton: false,
                timer: 3500,
              });
              setTimeout(function () {
                location.reload();
              }, 4000);
            } else
              this.$swal.fire({
                position: "top-end",
                icon: "warning",
                title: response.data.message,
                showConfirmButton: false,
                timer: 2500,
              });
          })
          .catch(() => {
            // not caught here (earlier)
            this.$swal.fire({
              position: "top-end",
              icon: "error",
              title: "something go wrong",
              showConfirmButton: false,
              timer: 2500,
            });
          });
      }
    },

    async DownloadResume() {
      const response = await axios
        .get("https://ipapi.co/json/")
        .then((response) => {
          this.ip_address = response.data.ip;
          this.city = response.data.city;
          this.region = response.data.region;
          this.country_name = response.data.country_name;
        });
      console.log(this.ip_address);
      const res = await axios.post(
        "https://ossamabottelegram.herokuapp.com/api/UserDownloader",
        {
          ip: this.ip_address,
          city: this.city,
          region: this.region,
          country_name: this.country_name,
        }
      );
      return res + response;
    },
  },
};
</script>
