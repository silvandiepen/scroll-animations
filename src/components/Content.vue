<template>
  <div :class="classes">
    <div :class="bemm('container')">
    <slot></slot></div>
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";

const props = defineProps({
  dark: {
    type: Boolean,
    default: false,
  },
});

const bemm = useBemm("content");

const classes = computed(() => {
  return [bemm(), props.dark ? bemm(null, "dark") : bemm(null, "light")];
});
</script>

<style lang="scss">
.content {
  width: 100%;
  padding: 4vw 0; 

  &__container {
    max-width: 96ch;
    margin: auto;
  }
  &--dark {
    background-color: #111;
    color: white;
  }
  p,
  .reveal {
    line-height: 1.5;
    margin: 0;
    & + p,
    & + .reveal {
      margin-top: 1em;
    }
  }

  .reveal {
    width: calc(100% + 4em);
    margin-left: -2em;
    border-radius: 0.5em;
  }

  p,h2,h3 {
    line-height: 1.75;
    transform: scale(0.8);

    view-timeline-name: --revealing-paragraph;
    view-timeline-axis: block;

    animation:  linear paragraph both;
    animation-timeline: --revealing-paragraph;
    animation-range: entry 0% cover 25%;

    opacity: 0.5;
  }
  @at-root {
    @keyframes paragraph {
      to {
        transform: scale(1);
        opacity: 1;
      }
    }
  }
}
</style>
