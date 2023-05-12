<template>
  <section id="survey-section">
    <div class="background">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>

    <div class="survey-container">
      <h3>Customer Surveys</h3>
      <div class="arrow arrow-left">
        <svg
          width="60"
          height="60"
          viewBox="0 0 60 60"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle
            cx="30"
            cy="30"
            r="28"
            fill="white"
            fill-opacity="0.4"
            stroke="#404040"
            stroke-width="4"
          />
          <line
            x1="2"
            y1="-2"
            x2="18.4827"
            y2="-2"
            transform="matrix(-0.781148 0.624346 -0.579146 -0.815224 35 18)"
            stroke="#404040"
            stroke-width="4"
            stroke-linecap="round"
          />
          <path
            d="M35 41L23.5 32"
            stroke="#404040"
            stroke-width="4"
            stroke-linecap="round"
          />
        </svg>
      </div>
      <div class="suvey-carousel">
        <div
          :class="[activeslide === 1 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            It's difficult to complete and sign batch records in laminar flow
            hoods and accessing supervisors or QA people in clean-room
            environments is also challenging.
            <br /><br />
            Recorded footage is becoming more common in pharma for deviations
            and investigations, helping QA people to confirm without the need to
            enter the facility.
            <br /><br />
            The recorded footage and calling somebody instantly to show what is
            happening at the same time sounds like the main benefits.
            <b>Sounds very futuristic and up and-coming</b>, the next step; I
            thought CCTV was new but... <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Manufacturing Manager, Insmed</b>
          </p>
        </div>

        <div
          :class="[activeslide === 2 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            There's a communication barrier between clinical and non-clinical
            sides due to specialized language.
            <br /><br />
            Oversight is crucial, but small companies may not have resources for
            dedicated teams. Electronic documents provide some oversight, but
            there's a lack of awareness about on-site processes.
            <br /><br />
            Virtual visits could improve efficiency and save time in clinical
            trials.
            <b>Great tool with great potential of using in clinical trials.</b>
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- VP Clinical, Ultrageny</b>
          </p>
        </div>

        <div
          :class="[activeslide === 3 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            Very interesting, beautiful and
            <b
              >effective in a lot of lab and manufacturing operational
              settings</b
            >. <br /><br />
            In a research lab, it is to always disorganized to take notes,
            information is scattered, so it would be very useful. Accessing
            videos, notes from dashboard and able to make calls from people in
            one room to other rooms in labs and manufacturing areas are very
            useful. Recorded video for just opening or closing a valve can be
            very helpful to capture certain information. It is like the walkie
            talkie which is used in certain facilities but definitely much
            better with video and dashboard.
            <br /><br />
            I can see it’s usage in many companies around and nearby.
            <b>This can be very useful for all the big pharma</b>, including
            vaccine research and companies. <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Senior Scientist, Noblegen</b>
          </p>
        </div>

        <div
          :class="[activeslide === 4 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            Some people wait to write notes or document issues because they
            don't have access to a computer near equipment. It can be
            distracting and slowing down the process.<br /><br />

            Live demonstrations are more useful for understanding and
            troubleshooting issues. Remote access can help with this, especially
            for larger companies. <br /><br />

            Visual access can be helpful for supervisors. Activity videos and
            voice-guided workflows can make things more efficient by providing
            access to information at the point of activity.
            <br /><br />
            So I think it’s very good.
            <b>It can make you more efficient, especially categorized notes</b>.
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Manufacturing Supervisor, Lonza</b>
          </p>
        </div>

        <div
          :class="[activeslide === 5 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            As a summary, I can see its utility in laboratory settings
            especially for monitoring if you are required to work at various
            locations and to monitor your students or interns for example.
            <br /><br />
            <b>It is definitely very useful to record your workflow</b> or your
            work-steps for future referral by other people in the lab.
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Research Scientist, A*Star</b>
          </p>
        </div>

        <div
          :class="[activeslide === 6 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            Having a readily available protocol in a lab is useful, but there's
            room for improvement. Real-time data capture and visual aids are
            critical for research progress tracking, and data capture on the
            spot is beneficial.
            <br /><br />
            Real-time feedback is essential for supervision, particularly for
            sensitive procedures. This technology could also aid remote auditing
            during Covid times and would benefit others.
            <br /><br />
            <b>
              I wish I had this kind of technology in my laboratory as I was
              doing my PhD.
            </b>
            It cannot be overstated how this kind of thing would really help
            other people. <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Post Doc. Research Scientist, University of Texas</b>
          </p>
        </div>

        <div
          :class="[activeslide === 7 ? 'survey-card active' : 'survey-card']"
        >
          <blockquote class="survey-text">
            In these times of social distancing due to Covid, it's difficult to
            train PhD students in person. Video feedback becomes important,
            especially for hands-on activities in biology labs.
            <br /><br />
            This kind of technology would be very useful to train people and
            fill the gaps.
            <br /><br />
            <b>
              It could even save costs on reagents by allowing for supervision
              to ensure things are done correctly the first time.
            </b>
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Post Doc. Research Scientist, University of Texas</b>
          </p>
        </div>
      </div>
      <div class="arrow arrow-right">
        <svg
          width="60"
          height="60"
          viewBox="0 0 60 60"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle
            cx="30"
            cy="30"
            r="28"
            transform="matrix(-1 0 0 1 60 0)"
            fill="white"
            fill-opacity="0.4"
            stroke="#404040"
            stroke-width="4"
          />
          <line
            x1="2"
            y1="-2"
            x2="18.4827"
            y2="-2"
            transform="matrix(0.781148 0.624346 0.579146 -0.815224 25 18)"
            stroke="#404040"
            stroke-width="4"
            stroke-linecap="round"
          />
          <path
            d="M25 41L36.5 32"
            stroke="#404040"
            stroke-width="4"
            stroke-linecap="round"
          />
        </svg>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SurveySection",
};
</script>

<style>
#survey-section {
  position: relative;
  width: 100vw;
}

.survey-container {
  padding: 8rem 0;
  width: 100%;
  display: grid;
  place-items: center;
  overflow-x: hidden;
}

.arrow {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 2;
  cursor: pointer;
  border: none;
  outline: none;
  color: white;
  -webkit-user-select: none;
}

.arrow-left {
  left: 1rem;
}

.arrow-right {
  right: 1rem;
}

.suvey-carousel {
  /* width: 100%; */
  height: 100%;
  display: flex;
  gap: 4rem;
  overflow-x: auto;
  padding-top: 2rem;
}

.survey-card {
  background: rgba(255, 255, 255, 0.6);
  backdrop-filter: blur(
    6px
  ); /* Note: backdrop-filter has minimal browser support */
  width: min(70ch, 55vw);
  border-radius: 12px;
  padding: 4rem;
}

.survey-text {
  margin-block: 0;
  margin-inline: 0;
  position: relative;
  font-style: italic;
  font-weight: 300;
}

.survey-text b {
  font-weight: 600;
}

.survey-text:before,
.survey-text:after {
  content: "\201C";
  position: absolute;
  font-size: 40px;
  line-height: 1;
  color: #757f9a;
  font-style: normal;
}

.survey-text:before {
  top: -1rem;
  left: -1.5rem;
}

.survey-text:after {
  content: "\201D";
  right: -1.5rem;
  bottom: 0.5rem;
}

/* ---------------------ANIMATED BACKGROUND---------------------- */

@keyframes move {
  100% {
    transform: translate3d(0, 0, 1px) rotate(360deg);
  }
}

.background {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;

  background: linear-gradient(
    262.86deg,
    #f3c2ff 2.68%,
    #c3c2ff 33.81%,
    #c2f4ff 96.08%
  );
  overflow: hidden;
  z-index: -1;
}

.background span {
  width: 26vmin;
  height: 26vmin;
  border-radius: 26vmin;
  backface-visibility: hidden;
  position: absolute;
  animation: move;
  animation-duration: 26;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}

.background span:nth-child(0) {
  color: #f89ffe;
  top: 37%;
  left: 15%;
  animation-duration: 168s;
  animation-delay: -202s;
  transform-origin: -15vw -14vh;
  box-shadow: -52vmin 0 6.713293931415641vmin currentColor;
}
.background span:nth-child(1) {
  color: #f89ffe;
  top: 82%;
  left: 69%;
  animation-duration: 11s;
  animation-delay: -61s;
  transform-origin: 19vw -15vh;
  box-shadow: -52vmin 0 6.536799427601847vmin currentColor;
}
.background span:nth-child(2) {
  color: #bd9afe;
  top: 69%;
  left: 77%;
  animation-duration: 149s;
  animation-delay: -154s;
  transform-origin: -9vw -11vh;
  box-shadow: 52vmin 0 7.005065505127338vmin currentColor;
}
.background span:nth-child(3) {
  color: #86aefe;
  top: 18%;
  left: 66%;
  animation-duration: 21s;
  animation-delay: -192s;
  transform-origin: -2vw 7vh;
  box-shadow: 52vmin 0 7.08204439509843vmin currentColor;
}
.background span:nth-child(4) {
  color: #f89ffe;
  top: 60%;
  left: 53%;
  animation-duration: 183s;
  animation-delay: -193s;
  transform-origin: 3vw -1vh;
  box-shadow: -52vmin 0 6.700348473439327vmin currentColor;
}
.background span:nth-child(5) {
  color: #86aefe;
  top: 12%;
  left: 32%;
  animation-duration: 71s;
  animation-delay: -240s;
  transform-origin: 18vw 13vh;
  box-shadow: 52vmin 0 6.851975471364639vmin currentColor;
}
.background span:nth-child(6) {
  color: #f89ffe;
  top: 69%;
  left: 7%;
  animation-duration: 169s;
  animation-delay: -111s;
  transform-origin: 14vw 5vh;
  box-shadow: -52vmin 0 6.802222855865738vmin currentColor;
}
.background span:nth-child(7) {
  color: #86aefe;
  top: 69%;
  left: 93%;
  animation-duration: 138s;
  animation-delay: -185s;
  transform-origin: -13vw 19vh;
  box-shadow: -52vmin 0 6.523249492134296vmin currentColor;
}
.background span:nth-child(8) {
  color: #bd9afe;
  top: 92%;
  left: 92%;
  animation-duration: 96s;
  animation-delay: -28s;
  transform-origin: -2vw 17vh;
  box-shadow: -52vmin 0 6.577381456250422vmin currentColor;
}
.background span:nth-child(9) {
  color: #f89ffe;
  top: 92%;
  left: 99%;
  animation-duration: 46s;
  animation-delay: -75s;
  transform-origin: 2vw 19vh;
  box-shadow: -52vmin 0 7.264463972654861vmin currentColor;
}
.background span:nth-child(10) {
  color: #86aefe;
  top: 97%;
  left: 95%;
  animation-duration: 162s;
  animation-delay: -86s;
  transform-origin: 25vw 25vh;
  box-shadow: 52vmin 0 7.091350625108296vmin currentColor;
}
.background span:nth-child(11) {
  color: #f89ffe;
  top: 11%;
  left: 24%;
  animation-duration: 20s;
  animation-delay: -207s;
  transform-origin: 16vw -15vh;
  box-shadow: 52vmin 0 6.74545130161018vmin currentColor;
}
.background span:nth-child(12) {
  color: #bd9afe;
  top: 36%;
  left: 57%;
  animation-duration: 174s;
  animation-delay: -185s;
  transform-origin: -4vw -18vh;
  box-shadow: -52vmin 0 6.9171538520555345vmin currentColor;
}
.background span:nth-child(13) {
  color: #86aefe;
  top: 49%;
  left: 99%;
  animation-duration: 237s;
  animation-delay: -34s;
  transform-origin: -9vw 12vh;
  box-shadow: -52vmin 0 7.08652584266299vmin currentColor;
}

@media only screen and (min-width: 1025px) {
  .arrow-left {
    left: clamp(6rem, -14.571rem + 32.143vw, 24rem);
  }

  .arrow-right {
    right: clamp(6rem, -14.571rem + 32.143vw, 24rem);
  }
}
</style>
