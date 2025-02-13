<template>
  <div class="wrapper">
    <div class="content">
      <TheHeader />
      <ThePortfolio />
    </div>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import TheHeader from "@/components/TheHeader.vue";
import ThePortfolio from "@/components/ThePortfolio.vue";

gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  if (window.ScrollSmoother) {

    if (ScrollTrigger.isTouch !== 1) {
      gsap.registerPlugin(window.ScrollSmoother);
      window.ScrollSmoother.create({
        wrapper: ".wrapper",
        content: ".content",
        smooth: 1.5,
        effects: true,
      });

      gsap.fromTo('.hero-section', { opacity: 1 }, { 
        opacity: 0,
        scrollTrigger: {
          trigger: '.hero-section',
          start: 'center',
          end: '820',
          scrub: true
        }
      })

      let itemsL = gsap.utils.toArray('.gallery__left .gallery__item') as HTMLElement[]

      itemsL.forEach((item: HTMLElement) => {
        gsap.fromTo(item, { x: -100, opacity: 0 }, {
        opacity: 1,
        x: 0,
        scrollTrigger: {
          trigger: item,
          scrub: true
        }
      })
      })

      let itemsR = gsap.utils.toArray('.gallery__right .gallery__item') as HTMLElement[]

      itemsR.forEach((item: HTMLElement) => {
        gsap.fromTo(item, { x: 100, opacity: 0 }, {
        opacity: 1,
        x: 0,
        scrollTrigger: {
          trigger: item,
          scrub: true
        }
      })
      })
    }
    
  } else {
    console.error("❌ ScrollSmoother не найден!");
  }
});

</script>

<style scoped>

</style>
