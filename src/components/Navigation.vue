<template>
  <nav :class="classes">
    <ul :class="bemm('list')">
      <li :class="bemm('item')" v-for="item in items">
        <a :class="bemm('link')" :href="item.link">{{ item.label }}</a>
      </li>
    </ul>
  </nav>
</template>
<script lang="ts" setup>
import { computed } from "vue";
import { useBemm } from "bemm";
import { PropType } from "vue";

import { NavigationItem } from "./Navigation.model";

defineProps({
  items: {
    type: Array as PropType<NavigationItem[]>,
    default: [],
  },
});

const bemm = useBemm("navigation");

const classes = computed(() => {
  return [bemm()];
});
</script>

<style lang="scss">
.navigation {
  position: absolute;
  transform: translateY(-50vh);

  animation: showNavigation cubic-bezier(0,.75,.5,1.5) both;
  animation-timeline: scroll();
  animation-range: 0 50vh;

  &__list {
    display: flex;
    margin: 0;
    padding: 0;
  }
  &__item {
    display: block;
  }
  &__link {
    padding: 1em;
    display: block;
    color: inherit;
    text-decoration: none;
  }
}

@keyframes showNavigation {
  to {
    transform: translateY(0%);
  }
}
</style>
