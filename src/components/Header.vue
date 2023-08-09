<template>
  <div :class="classes">
    <div :class="bemm('background')"></div>
    <h1><slot></slot></h1>
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
  width: 100%;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  position: fixed;
  top: 0;
  height: 80vh;

  animation: headerSize linear both;
  animation-timeline: scroll();
  animation-range: 0 50vh;
  z-index: 3;
  display: flex;
  justify-content: flex-end;
  z-index: 5;
  overflow: clip;
  background-color: black;

  &__background {
    position: absolute;
    left: -1rem;
    top: -1rem;
    width: calc(100% + 2rem);
    height: calc(100% + 2rem);
    background-color: #666;
    background-size: cover;
    background-position: 0 50%;
    background-image: url(https://images.unsplash.com/photo-1595608216441-abc4557df27d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2340&q=80);
    animation: headerImage ease-in-out both;
    animation-timeline: scroll();
    animation-range: 0 50vh;
    filter:blur(0);
    opacity: 1;
  }
  h1 {
    text-shadow: 4px 4px 0 black, 4px 4px 100px black;
    font-size: 3em;
    margin: 0;
    position: absolute;
    left: 50%;
text-align: left;    transform: translateX(-50%);
    max-width: 70vw; 

    animation: headerTitle ease-in-out both;
    animation-timeline: scroll();
    animation-range: 0 50vh;
    span{
      font-weight: normal;
    }
  }
}

@keyframes headerSize {
  to {
    height: 80px;
    font-size: 1em;
    background-color: #111111;
    text-align: left;
  }
}
@keyframes headerImage {
  to {
    background-position: 0 50%;
    filter:blur(10px);
    opacity: .5;
  }
}
@keyframes headerTitle {
  to {
    font-size: 1.5em;
    left: 1em;
    transform: translateX(0%);
  }
}
</style>
