<template>
  <section id="application-section">
      <div class="boxed">
        <h3 class="center" data-aos="fade-up" data-aos-duration="600" data-aos-easing="ease-in-out">Your All-in-One
                    Documentation Solution</h3>
          <video class="video" poster="../assets/img/dgxp-video-poster-min.jpg" autoplay loop muted
                    data-aos="zoom-in" data-aos-duration="1400" data-aos-easing="ease-in-out" data-aos-delay="200">
            <!-- HTML 5 browsers will play one of these -->
            <source src="../assets/video/dgxp-layout-video.webm" type="video/webm" />
            <source src="../assets/video/dgxp-layout-video.mp4" type="video/mp4" />
            <img src="../assets/img/dgxp-video-poster-min.jpg" title="Your browser does not support the <video> tag">
        </video>
      </div>

      <div class="stacked">
          <div class="notes note2">
            <h4>Notes</h4>
          </div>

          <div class="notes note1">
            <h4>SOP</h4>
          </div>

          <div class="notes note3">
            <h4>Log<br> Books</h4>
          </div>

          <div class="notes note2">
            <h4>Protocols</h4>
          </div>

          <div class="notes note1">
            <h4>Batch<br> Records</h4>
          </div>

          <div class="notes note4">
            <h4>Check<br> Sheets</h4>
          </div>

          <div class="notes note1">
            <h4>Work<br> Orders</h4>
          </div>

          <div class="notes note2">
            <h4>Forms</h4>
          </div>
          <div class="notes note4">
            <h4>ELN</h4>
          </div>
      </div>
    </section>
</template>

<script>
export default {
    name: 'ApplicationSection'
}
</script>

<style>
   .video {
        width: 100%;
        border-radius: 8px;
    }

    .notes {
        /* background-repeat: no-repeat;
        background-size: contain;
        background-position: center center; */

        display: grid;
        place-items: center;
        width: clamp(40px, 90%, 140px);
        aspect-ratio: 1.2 / 1;

        --grad-angle: calc(206.22deg - var(--rotate));
        background: linear-gradient(var(--grad-angle), #f5d889 16.5%, #fcf8b0 96.74%);
        transform: rotate(var(--rotate));
    }

    .notes h4 {
        font-size: clamp(0.8rem, 1.2vw, 1rem);
        padding: 2em 0;
        text-align: center;

        --adjust: calc(-1 * var(--rotate));
        transform: rotate(var(--adjust));

    }

    .note1 {
        /* background-image: url("../assets/img/sticky-note1.svg"); */
        box-shadow: -2px 4px 4px rgba(0, 0, 0, 0.2);
        transform: rotate(0.01deg);
        --rotate: 0.01deg;
    }

    .note2 {
        /* background-image: url("../assets/img/sticky-note2.svg"); */
        box-shadow: 2px 4px 4px rgba(0, 0, 0, 0.2);
        --rotate: 2deg;
    }

    .note3 {
        /* background-image: url("../assets/img/sticky-note3.svg"); */
        box-shadow: -4px 3px 4px rgba(0, 0, 0, 0.2);
        --rotate: -3deg;
    }

    .note4 {
        /* background-image: url("../assets/img/sticky-note1.svg"); */
        box-shadow: -4px 3px 4px rgba(0, 0, 0, 0.2);
        --rotate: -0.6deg;
    }


    
    #application-section {
        padding: clamp(4rem, 12vw, 10rem) 0;
        background-color: var(--dark-bg);

        position: relative;
    }

    #application-section h3 {
        color: white;
    }

    #application-section .stacked {
        margin-top: clamp(2em, 4%, 4em);
    }


    @media only screen and (min-width: 1025px) {
        
      #application-section .stacked {
          margin-bottom: -12em;
      }

      .notes h4 {
          padding: 0.5em 1em;
      }

      .note1 {
          margin-bottom: 0.8rem;
      }

      .note2 {
          margin-top: 1.5rem;
      }

      .note3 {
          margin-top: 1rem;
          margin-bottom: 1rem;
      }

      .note4 {
          margin-top: 1.2rem;
      }
    }
</style>