<template>
  <div :class="props.class">
    <div
      v-for="(child, index) in children"
      :key="index"
      class="animate-blur"
      :style="{ animationDelay: `${props.delay * index}s` }"
    >
      <component :is="child" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, watchEffect, useSlots } from 'vue';

interface Props {
  duration?: number;
  delay?: number;
  blur?: string;
  yOffset?: number;
  class?: string;
}

const props = withDefaults(defineProps<Props>(), {
  duration: 1,
  delay: 0.2,
  blur: '20px',
  yOffset: 20,
});

const container = ref(null);
const children = ref<any>([]);
const slots = useSlots();

onMounted(() => {
  watchEffect(() => {
    children.value = slots.default ? slots.default() : [];
  });
});
</script>

<style scoped>
.animate-blur {
  opacity: 0;
  filter: blur(v-bind(props.blur));
  transform: translateY(v-bind(props.yOffset + 'px'));
  animation: blurReveal v-bind(props.duration + 's') ease-in-out forwards;
}

@keyframes blurReveal {
  to {
    opacity: 1;
    filter: blur(0px);
    transform: translateY(0);
  }
}
</style>