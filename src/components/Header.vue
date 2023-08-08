<template>
  <div :class="classes">
    <h1>Scroll Animation Playground</h1>
    <Navigation :items="navigationItems" />
  </div>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";
import { PropType } from "vue";
import Navigation from "./Navigation.vue";

enum RevealType {
  CENTER = "center",
}

const props = defineProps({
  type: {
    type: String as PropType<RevealType>,
    default: RevealType.CENTER,
  },
});

const navigationItems = [
  { label: "home", link: "#" },
  { label: "about", link: "#" },
  { label: "work", link: "#" },
  { label: "contact", link: "#" },
];

const bemm = useBemm("header");

const classes = computed(() => {
  return [bemm(), bemm(null, props.type)];
});
</script>

<style lang="scss">
.header {
  background-color: #666;
  background-size: 300vw 100%;
  background-position: 0 0;
  width: 100%;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  position: fixed;
  top: 0;
  height: 80vh;

  animation: toHeader linear both;
  animation-timeline: scroll();
  animation-range: 0 50vh;
  z-index: 3;
  display: flex; justify-content: flex-end;
  z-index: 5;
  h1 {
    text-shadow: 4px 4px 0 black, 4px 4px 100px black;
    font-size: 3em; margin: 0;
    white-space: nowrap;
    position: absolute;
    left: 50%;
    text-align: center;
    transform: translateX(-50%);

    animation: toTitle cubic-bezier(0,.75,.5,1.5) both;
    animation-timeline: scroll();
    animation-range: 0 50vh;
  }
}

@keyframes toHeader {
  to {
    height: 80px;
    font-size: 1em;
    background-color: #111111;
    text-align: left;
  }
}
@keyframes toTitle {
  to {
    font-size: 1.5em;
    left: 1em;
    transform: translateX(0%);
  }
}
</style>
