<template>
  <section id="benefits-section">
    <div class="boxed center">
      <h3
        class="center"
        data-aos="fade-up"
        data-aos-duration="600"
        data-aos-easing="ease-in-out"
      >
        Paperless Solutions for Academic Labs, CROs & Industry
      </h3>
      <div class="grid center">
        <div
          class="befefit-card"
          data-aos="fade-up"
          data-aos-duration="600"
          data-aos-easing="ease-in-out"
          data-aos-delay="400"
        >
          <img
            src="../assets/illustrations/benefits/reduce-paperwork.png"
            srcset="../assets/illustrations/benefits/reduce-paperwork.svg"
            alt="A man with paperwork"
            loading="lazy"
            class="ilustration"
          />
          <h4 class="center">Reduce Paperwork</h4>
        </div>

        <div
          class="befefit-card"
          data-aos="fade-up"
          data-aos-duration="600"
          data-aos-easing="ease-in-out"
          data-aos-delay="800"
        >
          <img
            src="../assets/illustrations/benefits/access-anywhere.png"
            srcset="../assets/illustrations/benefits/access-anywhere.svg"
            alt="A woman with Mobile and tablet"
            loading="lazy"
            class="ilustration"
          />
          <h4 class="center">Access from Anywhere</h4>
        </div>

        <div
          class="befefit-card"
          data-aos="fade-up"
          data-aos-duration="600"
          data-aos-easing="ease-in-out"
          data-aos-delay="800"
        >
          <img
            src="../assets/illustrations/benefits/overcome-human-error.png"
            srcset="../assets/illustrations/benefits/overcome-human-error.svg"
            alt="Two men touching large screen"
            loading="lazy"
            class="ilustration"
          />
          <h4 class="center">Overcome Humam Error</h4>
        </div>

        <div
          class="befefit-card"
          data-aos="fade-up"
          data-aos-duration="600"
          data-aos-easing="ease-in-out"
          data-aos-delay="1200"
        >
          <img
            src="../assets/illustrations/benefits/collaboration-real-time.png"
            srcset="../assets/illustrations/benefits/collaboration-real-time.svg"
            alt="A group of people using laptop, tablet and mobile screens"
            loading="lazy"
            class="ilustration"
          />
          <h4 class="center">Collaborate in Real Time</h4>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BenefitSection",
};
</script>

<style>
.ilustration {
  width: min(80vw, 300px);
}

#benefits-section {
  padding: clamp(4rem, 10vw, 8rem) 0;
}

#benefits-section .grid {
  gap: 4em;
}
</style>
