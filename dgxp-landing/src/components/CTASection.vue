<template>
  <section id="sign-up">
    <div class="boxed">
      <h3
        class="center"
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-easing="ease-in-out"
      >
        Create a Free Demo Account
      </h3>
      <form
        method="post"
        id="sign-up-form"
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-delay="300"
        data-aos-easing="ease-in-out"
      >
        <label>Work Email* </label>
        <input
          type="email"
          id="wEmail"
          name="email"
          placeholder="Your work email here..."
          pattern=".+@globex\.com"
          required
          v-model="workEmail"
        />
        <input
          type="button"
          id="signUp"
          value="SIGN UP"
          v-on:click="emailSignUp"
        />
      </form>
    </div>
  </section>
</template>

<script>
import axios from "axios";

export default {
  name: "CTASection",
  data() {
    return {
      workEmail: null,
    };
  },
  methods: {
    async emailSignUp() {
      let app = this;

      var reg =
        /^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;
      let email = app.workEmail;
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

<style>
#sign-up {
  background-color: #000;
  padding: clamp(4rem, 10vw, 8rem) 0;
  margin: 2rem 0;
  scroll-margin-top: clamp(2rem, 4vw, 4rem);
}

#sign-up h3 {
  color: white;
}

#sign-up-form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#sign-up-form input {
  font-size: clamp(1rem, 2vw, 1.2rem);
  padding: 0.6em 2em;
  border-radius: 8px;
}

#sign-up-form #wEmail {
  width: min(90%, 300px);
}

#sign-up-form input[type="button"],
#sign-up-form input[type="submit"] {
  margin-top: 1rem;
}
</style>
