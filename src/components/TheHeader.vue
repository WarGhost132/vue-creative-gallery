<template>
  <header class="hero-section">
    <img data-speed=".6" class="hero" src="@/assets/images/hero.png" alt="Hero Image">
    <div class="container">
      <div data-speed=".75" class="main-header">
        <h1 class="main-title">creative gallery</h1>
      </div>
    </div>
  </header>
</template>

<style>
.hero {
  width: calc(var(--index) * 36);
  position: absolute;
  left: 37vw;
  top: 8vh;
  z-index: -1;
}
.main-header {
  height: 100vh;
}
.main-title {
  font-size: calc(var(--index) * 8);
  position: absolute;
  width: min-content;
  bottom: 12vh;
  line-height: .9;
}
</style>
