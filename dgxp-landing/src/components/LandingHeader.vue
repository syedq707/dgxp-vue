<template>
  <header id="header">
    <div class="wide">
      <a href="https://digitalgxp.com/" class="logo">
        <img
          id="logo"
          src="../assets/logo/DGxP-Logo.png"
          alt="Digital GxP logo"
        />
      </a>

      <nav id="primary-menu" v-bind:class="{ active: active }">
        <ul>
          <li>
            <a class="navlinks" href="https://digitalgxp.com/">Home</a>
          </li>
          <li>
            <a class="navlinks" href="https://digitalgxp.com/blog/">Blog</a>
          </li>
          <li>
            <a class="navlinks" href="https://app.digitalgxp.com/login"
              >Login</a
            >
          </li>
          <li>
            <button class="primary btn">
              <a href="#cta-section">Try Now</a>
            </button>
          </li>
        </ul>
      </nav>

      <div
        id="toggle-btn"
        v-on:click="toggleMobileMenu"
        v-bind:class="{ active: active }"
      >
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "LandingHeader",
  data() {
    return {
      active: false,
    };
  },
  created() {
    if (typeof window !== "undefined") {
      window.addEventListener("scroll", this.handleScroll);
    }
  },
  unmounted() {
    if (typeof window !== "undefined") {
      window.removeEventListener("scroll", this.handleScroll);
    }
  },
  methods: {
    handleScroll() {
      if (
        document.body.scrollTop > 50 ||
        document.documentElement.scrollTop > 50
      ) {
        document.getElementById("header").classList.add("shrink");
      } else {
        document.getElementById("header").classList.remove("shrink");
      }
    },
    toggleMobileMenu() {
      const navlinks = document.querySelectorAll(".navlinks");

      this.active = !this.active;

      // Animate Nav Text
      navlinks.forEach((link, index) => {
        if (link.style.animation) {
          link.style.animation = ``;
        } else {
          link.style.animation = `navLinksFade 0.5s ease backwards ${
            index / 6 + 0.4
          }s`;
        }
      });
    },
  },
};
</script>

<style>
/*---------------------------------  Custom Element Styling  ----------------------------*/

.logo img {
  width: 80px;
  height: auto;
  transition: all 0.2s ease-in;
}

.shrink .logo img {
  width: 60px;
  height: auto;
}

/* Mobile Menu & Burger Icon Styling Here */

#toggle-btn {
  display: block;
}

#toggle-btn div {
  width: 25px;
  height: 2px;
  background-color: #000;
  margin: 5px;

  transition: all 0.3s ease-in-out 0.3s;
  z-index: 3000;
}

#toggle-btn.active div {
  background-color: #fff;
}

#toggle-btn.active .line1 {
  transform: rotate(-45deg) translate(-5px, 6px);
}

#toggle-btn.active .line2 {
  opacity: 0;
}

#toggle-btn.active .line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}

header {
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: stretch;

  transition: all 0.2s ease-in;
  width: 100%;
  padding: 1rem 0;
  z-index: 2000;
}

header.shrink {
  padding: 0.5rem 0;
  background-color: #000;
}

header.shrink #toggle-btn div {
  background-color: #fff;
}

header .wide {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

nav#primary-menu ul {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;

  gap: 4rem;
  white-space: nowrap;
}

nav#primary-menu {
  position: absolute;
  top: 0;
  right: 0;
  /* width: clamp(10rem, 40%, 20rem); */
  transform: translateX(200%);
}

nav#primary-menu.active {
  background-color: #000;
  padding: 20% 10%;
  transform: translateX(0);
  transition: all 0.6 ease-in-out;
}

nav#primary-menu.active a.navlinks {
  color: #fff;
}

header button.btn {
   font-size: 1rem;
   white-space: nowrap;
}

/* nav#primary-menu ul li,
    nav#primary-menu ul li a {
        width: fit-content;
    } */

/*---------------------------------  CSS Animations ----------------------------*/

@keyframes navLinksFade {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }

  to {
    opacity: 1;
    transform: translateX(0px);
  }
}

@media only screen and (min-width: 1025px) {
  header #toggle-btn {
    display: none;
  }

  nav#primary-menu {
    position: static;
    transform: translate(0);
  }

  nav#primary-menu ul {
    flex-direction: row;
  }
}
</style>
