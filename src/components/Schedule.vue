<template>
  <section class="section">
    <div class="schedule-container">
      <h3 class="title">Schedule</h3>
      <div class="list">
        <p>Practice 1 : 28 August 2022 - 15h</p>
        <p>Practice 2 : 28 August 2022 - 15h</p>
        <p>Practice 3 : 28 August 2022 - 15h</p>
      </div>
      <div class="img"></div>
      <div class="img2"></div>
      <p class="qualification">Qualification : 28 August 2022 - 15h</p>
      <p class="race">Race Day : 28 August 2022 - 15h</p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section {
  padding: 3rem;
}
.schedule-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1.3fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 1rem;
  grid-auto-flow: row;
  grid-template-areas:
    "title title title"
    "list img qualification"
    "list img2 race";
}

.title {
  grid-area: title;
  justify-self: start;
  font-size: $-text-extra-large;
  text-transform: uppercase;
}

.list {
  grid-area: list;
}

.img {
  grid-area: img;
  background-color: grey;
}

.img2 {
  grid-area: img2;
  background-color: grey;
}

.qualification {
  grid-area: qualification;
}

.race {
  grid-area: race;
}

</style>
