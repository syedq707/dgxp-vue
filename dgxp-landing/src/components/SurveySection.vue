<template>
  <section id="testimonials">
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
      <h3 class="center">What People Are Saying</h3>
      <div class="arrow arrow-left" @click="prevSlide">
        <svg
          width="60"
          height="60"
          viewBox="0 0 60 60"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_b_757_2)">
            <circle cx="30" cy="30" r="30" fill="white" fill-opacity="0.4" />
            <circle cx="30" cy="30" r="28" stroke="#404040" stroke-width="4" />
          </g>
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
          <defs>
            <filter
              id="filter0_b_757_2"
              x="-6"
              y="-6"
              width="72"
              height="72"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feGaussianBlur in="BackgroundImageFix" stdDeviation="3" />
              <feComposite
                in2="SourceAlpha"
                operator="in"
                result="effect1_backgroundBlur_757_2"
              />
              <feBlend
                mode="normal"
                in="SourceGraphic"
                in2="effect1_backgroundBlur_757_2"
                result="shape"
              />
            </filter>
          </defs>
        </svg>
      </div>
      <div class="suvey-carousel">
        <div
          :class="[
            'survey-card',
            { active: activeslide === 1 },
            { left: activeslide === 15 },
            { right: activeslide === 2 },
          ]"
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
          :class="[
            'survey-card',
            { active: activeslide === 2 },
            { left: activeslide === 1 },
            { right: activeslide === 3 },
          ]"
        >
          <blockquote class="survey-text">
            In general, there is a communication barrier between the clinical
            and non-clinical sides due to language differences and a gap in
            understanding reports. Employers value close oversight but it may be
            challenging for small companies to dedicate a whole team to it.
            <br /><br />
            Electronic oversight based on reports is insufficient, as critical
            on-site processes often go unnoticed. This technology benefits
            oversight in pharmaceutical companies of all sizes, providing timely
            information and saving time. Virtual visits can revolutionize
            clinical trials, eliminating the need for physical site visits and
            unnecessary travel time.
            <b> Great tool with great potential of using in clinical trials.</b>
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- VP Clinical, Ultragenyx</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 3 },
            { left: activeslide === 2 },
            { right: activeslide === 4 },
          ]"
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
          :class="[
            'survey-card',
            { active: activeslide === 4 },
            { left: activeslide === 3 },
            { right: activeslide === 5 },
          ]"
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
          :class="[
            'survey-card',
            { active: activeslide === 5 },
            { left: activeslide === 4 },
            { right: activeslide === 6 },
          ]"
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
          :class="[
            'survey-card',
            { active: activeslide === 6 },
            { left: activeslide === 5 },
            { right: activeslide === 7 },
          ]"
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
          :class="[
            'survey-card',
            { active: activeslide === 7 },
            { left: activeslide === 6 },
            { right: activeslide === 8 },
          ]"
        >
          <blockquote class="survey-text">
            Physical movement is a problem in pharma manufacturing, especially
            between clean-rooms and suites. Electronic documentation is fixed to
            computer terminals, but
            <b> if accessed from a tab, the problem is solved.</b>
            <br /><br />
            Real-time supervision, troubleshooting, and guidance are crucial.
            Communication challenges within cleanrooms hinder collaboration.
            Streamlined document sharing and voice-based interactions would be
            valuable.
            <b
              >Integration with batch records and automated user authentication
              simplify processes.</b
            >
            <br /><br />
            POV streaming and monitoring from cleanroom operations would greatly
            help to supercise, without the need to go inside. Auditors can sit
            in one meeting room and walk the floor and whole process without
            moving. <b>It's useful from day one.</b> <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- QA Manager, Amgen</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 8 },
            { left: activeslide === 7 },
            { right: activeslide === 9 },
          ]"
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
            <b>- Post Doc. Research Scientist, University of Cambridge</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 9 },
            { left: activeslide === 8 },
            { right: activeslide === 10 },
          ]"
        >
          <blockquote class="survey-text">
            We're digitizing laboratories for enhanced online operations.
            Portable and interconnected devices are paving the way for a more
            online-oriented future.
            <br /><br />
            Laboratory techniques involve complex physical handling, including
            sampling, protocol checks, and processing. It's not as
            straightforward as computer-based tasks from 20 years ago.
            <br /><br />
            <b>So, having this device would greatly benefit customers,</b> as
            videos are more effective than any technical literature. Our
            industry has to be digital but it takes ages.
          </blockquote>
          <p class="survey-title">
            <b>- Director, Auxilab</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 10 },
            { left: activeslide === 9 },
            { right: activeslide === 11 },
          ]"
        >
          <blockquote class="survey-text">
            Prefer automated data-capturing, trending, and detection solutions
            like paperless systems for efficient on-site note taking and
            information sharing with supervisors in real time.
            <b>Live hands-free streaming enhances usability.</b> <br /><br />
            Some auditors prefer physical on-site viewing, while others prefer
            virtual options. The regulatory authorities are starting to consider
            these solutions for monitoring on-site activities.
            <br /><br />
            <b
              >Early event detection, data capture are trending and other AI
              tools sounds useful in certain situations.</b
            >
          </blockquote>
          <p class="survey-title">
            <b>- QA Manager, GSK</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 11 },
            { left: activeslide === 10 },
            { right: activeslide === 12 },
          ]"
        >
          <blockquote class="survey-text">
            I strongly support the need for
            <b
              >supervision and monitoring to identify and rectify errors during
              execution.</b
            >
            Clients expect processes to be executed precisely as documented,
            minimizing deviations. <br /><br />
            Cell and gene therapy companies require close monitoring due to the
            physical handling involved. Bringing clients to the facility ensures
            correct procedures, but
            <b
              >monitoring could be a valuable service if confidentiality is
              maintained.</b
            >
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Contract Manufacturing Manager, Gilead</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 12 },
            { left: activeslide === 11 },
            { right: activeslide === 13 },
          ]"
        >
          <blockquote class="survey-text">
            Recording information from the floor is essential for certain
            process parameters. On-site professionals use tools like Excel,
            Delta V, or Pi Software to analyze and record data for later
            reference. Sometimes use personal phone to take video of activity or
            screen.
            <br /><br />
            Monitoring critical activities, such as column packing, is
            important. In restricted environments like during CoVid, streaming
            and monitoring the activities would be helpful.
            <b
              >Video recording can aid in references, remote training, and
              virtual audits.</b
            >
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Sr. Process Engineer, Abbvie</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 13 },
            { left: activeslide === 12 },
            { right: activeslide === 14 },
          ]"
        >
          <blockquote class="survey-text">
            I think it is interesting, there is definitely a need for this.
            <b>The dashboard might be very helpful</b> from a contract
            manufacturing perspective because the client or others can see.
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Process Technologist, Exyte</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 14 },
            { left: activeslide === 13 },
            { right: activeslide === 15 },
          ]"
        >
          <blockquote class="survey-text">
            Real-time note taking is crucial during experiments, but it can be
            time-consuming. Manual methods are currently used, but labs and
            manufacturing sectors are interested in a more efficient solution.
            <b>Video capture is the standout feature</b>, offering great value
            for customer experiments and internal quality control by documenting
            specific steps effectively. <br /><br />
            In this restricted travel situation during CoVid, these devices have
            potential benefits.
            <b
              >When combined with an Electronic Notebook plug-in, they offer
              convenient access to view notes and videos.</b
            >
            <br /><br />
            For inventory management, improved sample tracking is crucial. While
            older labs may still prefer local storage, newer companies are
            comfortable with cloud solutions.
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Sr. Scientist, Proteona</b>
          </p>
        </div>

        <div
          :class="[
            'survey-card',
            { active: activeslide === 15 },
            { left: activeslide === 14 },
            { right: activeslide === 1 },
          ]"
        >
          <blockquote class="survey-text">
            This is a core problem faced by benchtop scientists in biotech labs.
            While many use Electronic Notebooks, systematically documenting
            everything remains a challenge, especially for filing IND and NDA.
            Integration of platforms could greatly improve the process.
            Currently, data is scattered across multiple computers and software,
            making it difficult for others to understand. There is room for
            improvement in this area.
            <br /><br />
            So I think that AI and having voice memos would be the technologies
            of the future. People would start using this kind of things more and
            more. <b>Useful as a notebook, hotline, video, all in one.</b>
            <br /><br />
          </blockquote>
          <p class="survey-title">
            <b>- Senior Scientist, Shape Therapeutics</b>
          </p>
        </div>
      </div>

      <div class="arrow arrow-right" @click="nextSlide">
        <svg
          width="60"
          height="60"
          viewBox="0 0 60 60"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g filter="url(#filter0_b_757_3)">
            <circle
              cx="30"
              cy="30"
              r="30"
              transform="matrix(-1 0 0 1 60 0)"
              fill="white"
              fill-opacity="0.4"
            />
            <circle
              cx="30"
              cy="30"
              r="28"
              transform="matrix(-1 0 0 1 60 0)"
              stroke="#404040"
              stroke-width="4"
            />
          </g>
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
          <defs>
            <filter
              id="filter0_b_757_3"
              x="-8"
              y="-8"
              width="76"
              height="76"
              filterUnits="userSpaceOnUse"
              color-interpolation-filters="sRGB"
            >
              <feFlood flood-opacity="0" result="BackgroundImageFix" />
              <feGaussianBlur in="BackgroundImageFix" stdDeviation="4" />
              <feComposite
                in2="SourceAlpha"
                operator="in"
                result="effect1_backgroundBlur_757_3"
              />
              <feBlend
                mode="normal"
                in="SourceGraphic"
                in2="effect1_backgroundBlur_757_3"
                result="shape"
              />
            </filter>
          </defs>
        </svg>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SurveySection",
  data() {
    return {
      activeslide: 1, // Currently active slide
      totalSlides: 15, // Total number of slides
    };
  },
  methods: {
    // Function to handle click on the left arrow
    prevSlide() {
      if (this.activeslide > 1) {
        this.activeslide--;
      } else {
        this.activeslide = 15;
      }
    },
    // Function to handle click on the right arrow
    nextSlide() {
      if (this.activeslide < this.totalSlides) {
        this.activeslide++;
      } else {
        this.activeslide = 1;
      }
    },
  },
};
</script>

<style>
#testimonials {
  position: relative;
  width: 100vw;
}

.survey-container {
  padding: 8rem 0;
  width: 100%;
}

.arrow {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 4;
  cursor: pointer;
  border: none;
  outline: none;
  color: white;
  -webkit-user-select: none;
}

.arrow svg {
  width: clamp(12px, 8vw, 60px);
}

.arrow-left {
  left: 0.5em;
}

.arrow-right {
  right: 0.5em;
}

.suvey-carousel {
  /* display: flex;
  justify-content: center;
  align-items: center; */

  width: 100%;
  overflow: hidden;

  position: relative;
  display: grid;
  place-items: center;

  gap: 4rem;
  padding-top: 2rem;
}

.survey-card {
  flex-shrink: 0;
  background: rgba(255, 255, 255, 0.6);
  backdrop-filter: blur(
    6px
  ); /* Note: backdrop-filter has minimal browser support */
  width: min(70ch, 75vw);
  border-radius: 12px;
  padding: clamp(2rem, 4vw, 4rem);
  transition: all 0.4s ease-in-out;
  grid-row: 1 / 2;
  grid-column: 1/2;
  display: none;
}

.survey-card.active {
  z-index: 2;
  filter: none;
  transform: scale(1);
  display: block;
}

.survey-card.left {
  transform: translateX(110%) scale(0.8);
  display: block;
  filter: blur(2px);
}

.survey-card.right {
  transform: translateX(-110%) scale(0.8);
  display: block;
  filter: blur(2px);
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
