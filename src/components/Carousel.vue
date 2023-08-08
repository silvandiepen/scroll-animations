<template>
  <div :class="classes">
    <ul :class="bemm('list')">
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
});

const bemm = useBemm("carousel");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
:root {
  --carousel-image-size: 240px;
}
.carousel {
  left: 50%;
  position: relative;
  transform: translateX(-50%);
  width: 100vw;
  &__list {
    list-style: none;
    white-space: nowrap;
    max-width: calc(var(--carousel-image-size) * 6);
    overflow: scroll;
    scroll-snap-type: x mandatory;
    height: calc(var(--carousel-image-size) * 2.5);
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    padding: 0 calc(var(--carousel-image-size) * 2);
  }
  &__item {
    flex-shrink: 0;
    display: inline-block;
    width: var(--carousel-image-size);
    aspect-ratio: 1;
    scroll-snap-align: center;
    view-timeline-name: --item-in-view;
    view-timeline-axis: inline;
    animation: linear setIndex both;
    animation-timeline: --item-in-view;
    perspective: 50em;
  }

  &__image {
    width: 100%;
    height: auto;
    border-radius: 0.25em;
    animation: linear rotateImage both;
    animation-timeline: --item-in-view;
  }
}

@keyframes rotateImage {
  0% {
    transform: translateX(-50%) rotateY(-30deg);
    opacity: 0.15;
  }
  35% {
    opacity: 1;
    transform: translateX(0) rotateY(-15deg);
  }
  50% {
    opacity: 1;
    transform: rotateY(0deg) translateZ(1em) scale(1.25);
  }
  65% {
    opacity: 1;
    transform: translateX(0) rotateY(15deg);
  }
  100% {
    transform: translateX(50%) rotateY(30deg);
    opacity: 0.15;
  }
}
@keyframes setIndex {
  0% {
    z-index: 1;
  }
  50% {
    z-index: 10;
  }
  100% {
    z-index: 1;
  }
}
</style>
