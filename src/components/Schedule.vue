<template>
  <section class="section">
    <div class="schedule-container">
      <h3 class="title">Schedule</h3>
      <div class="list">
        <h4 class="bloc-title">Practice 1</h4>
        <p>28 August 2022 <span class="badge">15:00</span></p>
        <h4 class="bloc-title">Practice 2</h4>
        <p>28 August 2022 <span class="badge">15:00</span></p>
        <h4 class="bloc-title">Practice 3</h4>
        <p>28 August 2022 <span class="badge">15:00</span></p>
      </div>
      <div class="img"></div>
      <div class="img2"></div>
      <div class="qualification">
        <h4 class="bloc-title">Qualification</h4>
        <p>28 August 2022 - 15h</p>
      </div>
      <div class="race">
        <h4 class="bloc-title">Race</h4>
        <p>28 August 2022 - 15h</p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section {
  padding: 3rem;
  text-align: left;
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

.list,
.img,
.img2,
.qualification,
.race {
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.74);
  border-radius: 5px;
  padding: 16px;
}
.title {
  grid-area: title;
  justify-self: start;
  font-size: $-text-extra-large;
  text-transform: uppercase;
}

.list {
  grid-area: list;
  background-color: $-color-honey-flower;
}

.img {
  grid-area: img;
  background-color: $-color-shark;
}

.img2 {
  grid-area: img2;
  background-color: $-color-concrete;
}

.qualification {
  grid-area: qualification;
  background-color: $-color-electric-red;
}

.race {
  grid-area: race;
  background-color:  $-color-electric-red;
}

.badge {
  margin: 0 24px;
  padding: 4px 16px;
  background-color: $-color-electric-red;
  border-radius: 15px;
}
.bloc-title {
  font-size: $-text-large;
  margin: 8px 0;
}
</style>
