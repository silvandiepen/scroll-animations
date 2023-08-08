<template>
  <div :class="classes">
    <div :class="bemm('column')">
      <ul :class="bemm('list')">
        <li :class="bemm('item')" v-for="image in images[0]">
          <img :class="bemm('image')" :src="image.src" />
        </li>
      </ul>
    </div>
    <div :class="bemm('column')">
      <ul :class="bemm('list')">
        <li :class="bemm('item')" v-for="image in images[1]">
          <img :class="bemm('image')" :src="image.src" />
        </li>
      </ul>
    </div>
    <div :class="bemm('column')">
      <ul :class="bemm('list')">
        <li :class="bemm('item')" v-for="image in images[2]">
          <img :class="bemm('image')" :src="image.src" />
        </li>
      </ul>
    </div>
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
      }[][]
    >,
  },
});

const bemm = useBemm("image-columns");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
:root {
  --carousel-image-size: 240px;
}
.image-columns {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  width: 100%;
  margin: 0 auto;
  position: relative;
  scroll-timeline-name: --squareTimeline;

  &__column {
    display: flex;
    flex-direction: column;
    animation: adjustPositionReverse linear forwards;
    animation-timeline: view();
    &:nth-child(odd) {
      animation: adjustPosition linear forwards;
      animation-timeline: view();
      flex-direction: column-reverse;
    }
  }
  &__list {
    gap: 2em;
    display: flex;
    flex-direction: column;
  }
  &__item {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__image {
    display: block;
    max-height: 100%;
    border-radius: 0.5em;
    height: 50vh;
    animation: imageIn linear forwards, imageOut linear forwards;
    animation-timeline: view();
    animation-range: entry 20%, exit 20%;
    transform: scale(0);
    opacity: 0; 
}
}

@keyframes imageIn {
  to {
    transform: scale(1);
    opacity: 1;
  }
}
@keyframes imageOut {
  to {
    transform: scale(0);
    opacity: 0; 
  }
}

@keyframes adjustPosition {
  0% {
    transform: translateY(calc(100% - 100vh));
  }
  100% {
    transform: translateY(calc(-100% + 100vh));
  }
}
@keyframes adjustPositionReverse {
  100% {
    transform: translateY(calc(100% - 100vh));
  }
  0% {
    transform: translateY(calc(-100% + 100vh));
  }
}
</style>
