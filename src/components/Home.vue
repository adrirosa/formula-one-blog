<script></script>

<template>
  <div class="home">
    <div class="race-infos">
      <h1>Next race</h1>
      <h2>Formula 1 Rolex Belgian Grand Prix</h2>

      <p>28 Aug 2022</p>
    </div>

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
  <div class="overlay"></div>
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
}
.credit {
  position: absolute;
  bottom: 0;
  font-size: 12px;
  color: rgb(157, 157, 157);
}
</style>
