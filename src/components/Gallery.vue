<template>
  <div :class="classes">
    <ul :class="bemm('list')">
      <li v-if="intro" :class="[bemm('item'), bemm('item', 'intro')]">
        <h3>{{ intro }}</h3>
      </li>

      <li :class="bemm('item')" v-for="image in images">
        <img :class="bemm('image')" :src="image.src" />
      </li>
    </ul>
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";
import { PropType } from "vue";

defineProps({
  images: {
    type: Array as PropType<
      {
        src: string;
      }[]
    >,
  },
  intro: {
    type: String,
    default: "",
  },
});

const bemm = useBemm("gallery");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
:root {
  --carousel-image-size: 240px;
}
body{
  width: 100vw; overflow-x: hidden;
}
.gallery {
  background-color: black;
  padding: 4vw 0;

  height: 400vh;
  overflow: visible;
  view-timeline-name: --gallery;
  view-timeline-axis: block;

  &__container {
    height: 100vh;
    width: 100vw;
    position: sticky;
    top: 0;
    width: 100vw;
    overflow-x: hidden;
  }
  &__list {
    position: sticky;
    top: 0;
    height: 100vh;
    width: 250vmax;
    will-change: transform;
    animation: linear move forwards;
    animation-timeline: --gallery;
    animation-range: contain 0% contain 100%;

    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding: 50px 10vw;
    gap: 2em;
  }
  &__item {
    height: 80vh;
    width: auto;
    max-width: 100%;
    object-fit: cover;
    &--intro {
      min-width: 50vw;
      color: white;
      padding: 4vw;
      font-size: 2vw;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }

  &__image {
    border-radius: 0.5em;
  }
}
@keyframes move {
  100% {
    transform: translateX(calc(-100% + -100vw));
    left: 0px;
  }
}
</style>
