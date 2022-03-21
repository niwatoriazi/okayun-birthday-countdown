<script setup>
import CountDownWrapper from "./components/CountDownWrapper.vue";
</script>

<template>
  <div id="bg-video" class="w-screen h-screen fixed filter blur-md">
    <video
      class="w-full h-full object-cover"
      src="./assets/okayun-birthday-countdown-back-video.mp4"
      poster="./assets/okayun-birthday-countdown-back-video_poster.webp"
      autoplay
      muted
      playsinline
      loop
    ></video>
  </div>
  <CountDownWrapper></CountDownWrapper>
  <div id="page-title-wrapper" class="display-width">
    <p id="page-title" class="text-sm lg:text-base text-center text-white">
      おかゆんお誕生日カウントダウン(非公式)
    </p>
  </div>
  <div id="copy-wright-wrapper" class="display-width">
    <a
      href="https://twitter.com/niwatoriazi"
      target="_blank"
      id="copy-right"
      class="text-xs lg:text-base text-center underline text-white"
      >©2021 にわとりあじ</a
    >
  </div>
  <div
    id="frame"
    class="fixed inset-0 w-screen h-screen pointer-events-none"
  ></div>
  <a
    href="https://niwatoriazi.github.io/korosan-birthday-countdown/"
    id="korosan-counter-link"
    class="fixed right-10 bottom-38 lg:right-20 lg:bottom-76 transform hover:-rotate-6 hover:scale-110 duration-200"
  >
    <img src="./assets/1f950.svg" class="w-16 lg:w-24" />
  </a>
  <a
    href="https://twitter.com/nekomataokayu"
    id="twitter-share-link"
    target="_blank"
    class="fixed right-10 bottom-24 lg:right-20 lg:bottom-48 transform hover:-rotate-6 hover:scale-110 duration-200"
  >
    <img
      class="w-16 lg:w-24"
      src="./assets/2021Twitter_logo-blue.png"
      alt="twitter-logo"
    />
  </a>
  <a
    href="https://www.youtube.com/channel/UCvaTdHTWBGv3MKj3KVqJVCw"
    id="youtube-channel-link"
    target="_blank"
    class="fixed right-10 bottom-10 lg:right-20 lg:bottom-20 transform hover:-rotate-6 hover:scale-110 duration-200"
  >
    <img
      class="w-16 lg:w-24"
      src="./assets/youtube_social_icon_red.webp"
      alt="youtube-logo"
    />
  </a>
</template>

<style lang="scss">
@import url(https://fonts.googleapis.com/css2?family=DotGothic16&family=Hachi+Maru+Pop&family=Press+Start+2P&display=swap);
@supports (-webkit-touch-callout: none) {
  #bg-video {
    height: -webkit-fill-available;
  }
  #frame {
    height: -webkit-fill-available;
  }
  #count-down-wrapper {
    height: -webkit-fill-available;
    overflow: hidden;
  }
}
body {
  background-color: #b190fc;
  cursor: url(./assets/onigiri.png), auto;
}
#party {
  z-index: -1;
  cursor: url(./assets/onigiri.png), auto;
}
.z-layer:not(:first-child) {
  color: #455a64;
}
#page-title-wrapper {
  z-index: 1;
  width: 100vw;
  height: 50px;
  @media (orientation: portrait) {
    height: 30px;
  }
  top: 0px;
  position: fixed;
  display: grid;
  place-content: center;
  #page-title {
    font-family: "Hachi Maru Pop", cursive;
  }
}
#copy-wright-wrapper {
  z-index: 1;
  width: 100vw;
  height: 50px;
  @media (orientation: portrait) {
    height: 30px;
  }
  bottom: 0px;
  position: fixed;
  display: grid;
  place-content: center;
  #copy-right {
    cursor: url(./assets/negitoro-onigiri.png), pointer;
    font-family: "Hachi Maru Pop", cursive;
  }
}
#bg-video {
  z-index: -3;
}
#frame {
  border: solid 50px #b190fc;
  z-index: 0;
  @media (orientation: portrait) {
    border: solid 30px #b190fc;
  }
}
#korosan-counter-link {
  cursor: url(./assets/negitoro-onigiri.png), pointer;
}
#twitter-share-link {
  cursor: url(./assets/negitoro-onigiri.png), pointer;
}
#youtube-channel-link {
  cursor: url(./assets/negitoro-onigiri.png), pointer;
}
</style>
