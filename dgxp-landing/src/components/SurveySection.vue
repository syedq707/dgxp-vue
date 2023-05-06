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
  height: 100vh;
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
</style>
