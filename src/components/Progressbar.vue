<template>
  <div :class="classes">
    <div :class="bemm('bar')"></div>
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";
// import { PropType } from "vue";

// enum RevealType {
//   CENTER = "center",
// }

// const props = defineProps({
//   type: {
//     type: String as PropType<RevealType>,
//     default: RevealType.CENTER,
//   },
// });

const bemm = useBemm("progress");

const classes = computed(() => {
  return [
    bemm(),
  ];
});
</script>

<style lang="scss">
.progress {
  z-index: 6;
  background-color: rgba(0, 0, 0, 0.25);
  width: 100vw;
  position: fixed;
  top: 0;
  height: 0.25em;
  left: 0;
  &__bar {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    background-color: red;
    width: 100%;
    transform: scale(0, 1);
    transform-origin: 0 0;
    animation: linear forwards scrollProgress;
    animation-duration: auto;
    animation-timeline: scroll(block nearest);
  }
}
@keyframes scrollProgress {
  from {
    transform: scale(0, 1);
  }
  to {
    transform: scale(1, 1);
  }
}
</style>
