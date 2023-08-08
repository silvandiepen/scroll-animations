<template>
  <div :class="classes">
    <img :src="src" />
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";
import { PropType } from "vue";

import { RevealType } from "./Reveal.model";

const props = defineProps({
  type: {
    type: String as PropType<RevealType>,
    default: RevealType.CENTER,
  },
  src: {
    type: String,
    default: "",
    required: true,
  },
});

const bemm = useBemm("reveal");

const classes = computed(() => {
  return [bemm(), bemm(null, props.type)];
});
</script>

<style lang="scss">
.reveal {
  img {
    margin: 0;
    width: 100%;
  }

  &--center {
    view-timeline-name: --revealing-image;
    view-timeline-axis: block;
    animation: linear reveal-center both;
    animation-timeline: --revealing-image;
    animation-range: entry 0% cover 50%;
    img {
      display: block;
    }
    @at-root {
      @keyframes reveal-center {
        0% {
          clip-path: inset(45% 20% 45% 20%);
        }
        100% {
          clip-path: inset(0% 0% 0% 0%);
        }
      }
    }
  }
  &--left {
    view-timeline-name: --revealing-image-left;
    view-timeline-axis: block;
    animation: cubic-bezier(0,.75,.5,1.5) reveal-left both;
    animation-timeline: --revealing-image-left;
    animation-range: entry 0% cover 50%;
    img {
        border-radius: .5em;
    }
    @at-root {
      @keyframes reveal-left {
        0% {
          clip-path: inset(0% 0% 0% 100%);
        }
        100% {
          clip-path: inset(0% 0% 0% 0%);
        }
      }
    }
  }
}
</style>
