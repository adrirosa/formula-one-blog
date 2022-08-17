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

      return `${days} days, ${hours} hours, ${minutes} minutes, ${seconds} seconds`;
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
  <div>{{ timeRemaining }}</div>
</template>
