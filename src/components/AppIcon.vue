<script setup lang="ts">
import { icons } from "@/assets/index.ts";
import { computed } from "vue";

const props = defineProps<{
  name: keyof typeof icons;
}>();

const iconComponent = computed(() => {
  return icons[props.name];
});
</script>

<template>
  <component :is="iconComponent"></component>
</template>
