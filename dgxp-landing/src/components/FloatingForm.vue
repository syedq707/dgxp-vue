<template>
    <form method="post" id="email-drop" v-bind:class="{show: showForm}">
            <h4>
                Drop Your Email for Demo
            </h4>
            <input type="email" id="email" pattern=".+@globex\.com" required v-model="emailForDemo">
            <input type="button" id="submit" value="SUBMIT" v-on:click="dropEmailForDemo">
    </form>
</template>

<script>
import axios from 'axios'

export default {
    name: 'FloatingForm',
    props: ['showForm'],
    data() {
        return {
            emailForDemo: null,
        }
    },
    methods: {

        dropEmailForDemo() {
            
            if (
                this.emailForDemo == null ||
                this.emailForDemo == ""
            ) {
                window.alert("Please Enter a valid email address!");
            } else {
                this.emailForDemo = this.emailForDemo.trim();
                let app = this;
                axios
                .post("/api/dropEmailForDemo", {
                    email: this.emailForDemo,
                })
                .then(function () {
                    // console.log(response);
                    // app.showLoginModal = true;
                    // app.showRegisterModal = false;
                    // app.$router.push("/login");
                    app.emailForDemo = "";
                    window.alert(
                    "Your Email address has been saved for Demo. We will contact you shortly. \n\n-Team Digital GxP"
                    );
                })
                .catch(function (error) {
                    console.log(error);
                });
            }
        },
    }
}
</script>

<style>

</style>