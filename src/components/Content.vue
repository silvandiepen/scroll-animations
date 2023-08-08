<template>
  <div :class="classes">
    <slot></slot>
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";

const bemm = useBemm("content");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
.content {
  width: 100%;
  max-width: 96ch;
  margin: auto;

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

  p {
    transform: scale(0.8);

    view-timeline-name: --revealing-paragraph;
    view-timeline-axis: block;

    animation: cubic-bezier(0,.75,.5,1.5) paragraph both;
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
