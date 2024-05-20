<script>
export default {
  data() {
    return {
      now: new Date(),
      raceDate: new Date("08/28/2022 15:00:00"),
    };
  },
  mounted() {
    setInterval(this.getCurrentDate.bind(this), 1000);
  },
  computed: {
    timeRemaining() {
      const remainingMilliseconds =
        this.raceDate.getTime() - this.now.getTime();

      const { days, hours, minutes, seconds } = this.convertMilliseconds(
        remainingMilliseconds
      );

      return { days, hours, minutes, seconds };
    },
  },
  methods: {
    getCurrentDate() {
      this.now = new Date();
    },
    convertMilliseconds(milliseconds) {
      let seconds = Math.floor(milliseconds / 1000);
      let minutes = Math.floor(seconds / 60);
      let hours = Math.floor(minutes / 60);
      let days = Math.floor(hours / 24);

      seconds = seconds % 60;
      minutes = minutes % 60;
      hours = hours % 24;

      return { days, hours, minutes, seconds };
    },
  },
};
</script>

<template>
<p>Coming in</p>
  <div class="countdown-container">
    <div class="countdown-card">
      <h2 class="countdown-timer">{{ timeRemaining.days }}</h2>
      <p class="countdown-label">days</p>
    </div>
    <div class="countdown-card">
      <h2 class="countdown-timer">
        {{ timeRemaining.hours.toString().padStart(2, "0") }}
      </h2>
      <p class="countdown-label">hours</p>
    </div>
    <div class="countdown-card">
      <h2 class="countdown-timer">
        {{ timeRemaining.minutes.toString().padStart(2, "0") }}
      </h2>
      <p class="countdown-label">minutes</p>
    </div>
    <div class="countdown-card">
      <h2 class="countdown-timer">
        {{ timeRemaining.seconds.toString().padStart(2, "0") }}
      </h2>
      <p class="countdown-label">seconds</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.countdown-container {
  display: flex;
  justify-content: center;
}
.countdown-card {
  display: flex;
  flex-direction: column;
  width: 88px;
  height: 120px;
  padding: 16px;
  margin: 0 8px;
  background-color: $-color-concrete;
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.74);
  border-radius: 5px;
  color: rgb(36, 36, 36);
}
.countdown-timer {
  margin: 0;
  font-size: 3em;
  font-weight: 700;
}
</style>
