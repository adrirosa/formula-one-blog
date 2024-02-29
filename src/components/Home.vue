<script>
import Countdown from "./Countdown.vue";
import Schedule from "./Schedule.vue";

export default {
  components: {
    Countdown,
    Schedule,
  },
  data() {
    return {
      isHover: false,
    };
  },
};
</script>

<template>
  <div class="home" @mouseenter="isHover = true" @mouseleave="isHover = false">
    <div class="race-infos" :class="{ hover: isHover }">
      <h1>Next race</h1>
      <p class="race-name">Formula 1 Rolex Belgian Grand Prix</p>

      <!-- <p>28 Aug 2022</p> -->
    </div>

    <Countdown />

    <span class="credit"
      >Photo by
      <a
        href="https://unsplash.com/@brondia?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText"
        >Alexandre Brondino</a
      >
      on
      <a
        href="https://unsplash.com/s/photos/f1-belgian?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText"
        >Unsplash</a
      >
    </span>
  </div>
  <div class="background"></div>
  <div class="overlay" :class="{ hover: isHover }"></div>

  <Schedule class="section" />
</template>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
  width: 100%;
  height: 100%;
  z-index: 10;
}
.background {
  top: 0;
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: url("../assets/img/f1-spa.jpg");
  background-size: cover;
}

.overlay {
  top: 0;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  transition: background-color 1s 0.3s;
}
.overlay.hover {
  background-color: rgba(0, 0, 0, 0.75);
}

.race-infos {
  transition: font-size 1s;
}
.race-infos.hover {
  font-size: xx-large;
}
.race-name {
  font-size: 2em;
}
.credit {
  position: absolute;
  bottom: 0;
  width: 100%;
  font-size: 12px;
  color: rgb(157, 157, 157);
}

</style>
