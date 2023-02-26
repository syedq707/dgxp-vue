<template>
  <form method="post" id="email-drop" v-bind:class="{ show: showForm }">
    <h4>Drop Your Email for Demo</h4>
    <input
      type="email"
      id="email"
      pattern=".+@globex\.com"
      required
      v-model="emailForDemo"
    />
    <input
      type="button"
      id="submit"
      value="SUBMIT"
      v-on:click="dropEmailForDemo"
    />
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: "FloatingForm",
  props: ["showForm"],
  data() {
    return {
      emailForDemo: null,
    };
  },
  methods: {
    async dropEmailForDemo() {
      let app = this;

      var reg =
        /^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;
      let email = app.emailForDemo;
      email = email.trim();
      if (email == null || email == "" || !reg.test(email)) {
        window.alert("Please Enter a valid email address!");
      } else {
        const api_url = "https://digitalgxp.com/email/subscribe/";

        let res = await axios
          .post(api_url, {
            email,
          })
          .then(function () {
            // console.log(response);
            // app.showLoginModal = true;
            // app.showRegisterModal = false;
            // app.$router.push("/login");
            // app.emailForDemo = "";
            window.alert(
              "Your Email address has been saved for Demo. We will contact you shortly. \n\n-Team Digital GxP"
            );
          })
          .catch(function (error) {
            console.log(error);
          });

        console.log(res);
      }
    },
  },
};
</script>

<style></style>
