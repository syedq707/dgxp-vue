<template>
  <!-- <div class="floating-btn">
        <form method="post" id="email-drop" v-bind:class="{show: showForm}">
            <h4>
                Drop Your Email for Demo
            </h4>
            <input type="email" id="email" pattern=".+@globex\.com" required v-model="emailForDemo">
            <input type="button" id="submit" value="SUBMIT" v-on:click="dropEmailForDemo">
        </form>

        <div>
            <button class="email-btn" v-on:click="showForm">
                <svg width="30" height="22" viewBox="0 0 30 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M13.8616 12.2119L13.0078 13.4452L13.0078 13.4452L13.8616 12.2119ZM16.1384 12.2119L16.9922 13.4452L16.9922 13.4452L16.1384 12.2119ZM4 3.5H26V0.5H4V3.5ZM26.5 4V18H29.5V4H26.5ZM26 18.5H4V21.5H26V18.5ZM3.5 18V4H0.5V18H3.5ZM4 18.5C3.72386 18.5 3.5 18.2761 3.5 18H0.5C0.5 19.933 2.067 21.5 4 21.5V18.5ZM26.5 18C26.5 18.2761 26.2761 18.5 26 18.5V21.5C27.933 21.5 29.5 19.933 29.5 18H26.5ZM26 3.5C26.2761 3.5 26.5 3.72386 26.5 4H29.5C29.5 2.067 27.933 0.5 26 0.5V3.5ZM4 0.5C2.067 0.5 0.5 2.067 0.5 4H3.5C3.5 3.72386 3.72386 3.5 4 3.5V0.5ZM1.14619 5.23329L13.0078 13.4452L14.7154 10.9786L2.85381 2.76671L1.14619 5.23329ZM16.9922 13.4452L28.8538 5.23329L27.1462 2.76671L15.2846 10.9786L16.9922 13.4452ZM13.0078 13.4452C14.2063 14.2749 15.7937 14.2749 16.9922 13.4452L15.2846 10.9786C15.1134 11.0971 14.8866 11.0971 14.7154 10.9786L13.0078 13.4452Z"
                        fill="white" />
                </svg>
            </button>
        </div>

    </div> -->
    <div>
            <button class="email-btn" v-on:click="showForm">
                <svg width="30" height="22" viewBox="0 0 30 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M13.8616 12.2119L13.0078 13.4452L13.0078 13.4452L13.8616 12.2119ZM16.1384 12.2119L16.9922 13.4452L16.9922 13.4452L16.1384 12.2119ZM4 3.5H26V0.5H4V3.5ZM26.5 4V18H29.5V4H26.5ZM26 18.5H4V21.5H26V18.5ZM3.5 18V4H0.5V18H3.5ZM4 18.5C3.72386 18.5 3.5 18.2761 3.5 18H0.5C0.5 19.933 2.067 21.5 4 21.5V18.5ZM26.5 18C26.5 18.2761 26.2761 18.5 26 18.5V21.5C27.933 21.5 29.5 19.933 29.5 18H26.5ZM26 3.5C26.2761 3.5 26.5 3.72386 26.5 4H29.5C29.5 2.067 27.933 0.5 26 0.5V3.5ZM4 0.5C2.067 0.5 0.5 2.067 0.5 4H3.5C3.5 3.72386 3.72386 3.5 4 3.5V0.5ZM1.14619 5.23329L13.0078 13.4452L14.7154 10.9786L2.85381 2.76671L1.14619 5.23329ZM16.9922 13.4452L28.8538 5.23329L27.1462 2.76671L15.2846 10.9786L16.9922 13.4452ZM13.0078 13.4452C14.2063 14.2749 15.7937 14.2749 16.9922 13.4452L15.2846 10.9786C15.1134 11.0971 14.8866 11.0971 14.7154 10.9786L13.0078 13.4452Z"
                        fill="white" />
                </svg>
            </button>
        </div>
</template>

<script>
export default {
    name: 'FloatingButton',
    methods: {
        showForm() {
            this.$emit('toggleShowForm');
        },
    }
}
</script>

<style>
  .floating-btn {
        display: flex;
        align-items: flex-end;
        gap: 0.5rem;

        position: fixed;
        bottom: 1rem;
        right: 1rem;
        z-index: 200;
    }

    #email-drop {
        display: none;
        background-color: #000;
        padding: clamp(1em, 2vw, 1.5em);
        border-radius: 8px;
        /* opacity: 0;
        transform: scaleY(0.2) translateX(100%);
        transition: all 0.3s ease-in-out; */
    }

    #email-drop.show {
        display: block;
        /* opacity: 1;
        transform: scaleY(1) translateX(0); */
    }

    #email-drop h4 {
        /* font-size: 1rem; */
        color: #fff;
        font-weight: normal;
    }

    @media only screen and (min-width: 1025px) {
         
        .floating-btn {
            bottom: 4rem;
            right: 6rem;
        }
     }
</style>