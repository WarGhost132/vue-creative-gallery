<template>
  <div class="portfolio">
    <div class="container">
      <main class="gallery">
        <div data-speed=".9" class="gallery__left">

          <img class="gallery__item" src="@/assets/images/work/1.jpg" alt="Artwork 1">
          <img class="gallery__item" src="@/assets/images/work/2.jpg" alt="Artwork 2">

          <div class="text-block gallery__item">
            <h2 class="text-block__h">
              Exploring the Boundaries of Creativity
            </h2>
            <p class="text-block__p">
              Dive into a world where art meets innovation. Our gallery showcases the finest works from emerging and established artists, blending traditional techniques with modern digital art.
            </p>
          </div>

          <img class="gallery__item" src="@/assets/images/work/6.jpg" alt="Artwork 6">

        </div>
        <div data-speed="1.1" class="gallery__right">

          <div class="text-block gallery__item">
            <h2 class="text-block__h">
              A Journey Through Visual Storytelling
            </h2>
            <p class="text-block__p">
              Each piece in our collection tells a unique story, capturing moments of beauty, emotion, and imagination. Experience the power of visual storytelling through our curated gallery.
            </p>
          </div>

          <img class="gallery__item" src="@/assets/images/work/4.jpg" alt="Artwork 4">
          <img class="gallery__item" src="@/assets/images/work/5.jpg" alt="Artwork 5">
          <img class="gallery__item" src="@/assets/images/work/3.jpg" alt="Artwork 3">

        </div>
      </main>
    </div>
  </div>
</template>

<style>
.gallery {
  display: flex;
  padding: calc(var(--index) * 8) 0;
}
.gallery > * {
  flex: 1;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.gallery__item {
  max-width: calc(var(--index) * 21);
  margin-bottom: var(--gallery-gap);
  max-height: 180vh;
  border-radius: 8px;
}
.gallery__left {
  margin-top: calc(var(--gallery-gap) * 1.75);
}
.gallery__right .gallery__item {
  margin: 0;
  margin-top: var(--gallery-gap);
}
.text-block {
  color: var(--color-text);
  position: relative;
}
.text-block__h {
  font-size: 2rem;
  line-height: 2.4rem;
  color: var(--color-header);
  margin-bottom: 1.5rem;
}
.text-block__p {
  line-height: 1.75;
}
</style>
