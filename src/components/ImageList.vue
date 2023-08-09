<template>
  <div :class="classes">
    <ul :class="bemm('list')">
      <li :class="bemm('item')" v-for="image in images">
        <figure :class="bemm('figure')">
        <img :class="bemm('image')" :src="image.src" />
    </figure>  <figcaption :class="bemm('caption')" >
        <h3>{{ image.title }}</h3>
        <p>{{ image.description  }}</p></figcaption>

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
        description: string;
        title: string;
      }[]
    >,
  },
});

const bemm = useBemm("image-list");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
:root {
  --carousel-image-size: 240px;
}
.image-list {
  &__list {
    gap: 2em;
    display: flex;
    flex-direction: column;
  }
  &__item {
    animation: itemIn linear forwards, itemOut linear forwards;
    animation-timeline: view();
    animation-range: entry, exit;
    max-height: 50vh;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 100%;
    align-items: center;
    justify-content: center;
  }

  &__image {
    display: block;
    max-height: 100%;
    border-radius: 0.5em;
    height: 500px;
  }
  &__caption{
    width: 320px;    
    animation: captionIn linear forwards, captionOut linear forwards;
    animation-timeline: view();
    animation-range: entry, exit;
    p{
        opacity: .75;
        line-height: 1.75;
    }
  }
}

@keyframes captionIn {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0%);
  }
}
@keyframes captionOut {
  0% {
    opacity: 1;
    transform: translateX(0%);
  }
  100% {
    opacity: 0;
    transform: translateX(100%);
  }
}
@keyframes itemIn {
  0% {
    opacity: 0;
    transform: translateY(100%);
    z-index: 0;
  }
  100% {
    opacity: 1;
    transform: translateY(0%);
    z-index: 3;
  }
}
@keyframes itemOut {
  0% {
    opacity: 1;
    transform: translateY(0%);
    z-index: 3;
  }
  100% {
    opacity: 0;
    transform: translateY(-100%);
    z-index: 0;
  }
}
</style>
