<script setup lang="ts">
withDefaults(defineProps<{ className?: string }>(), {
  className: "",
});
</script>

<template>
  <a
    href="#forma"
    :class="`group inline-flex items-center gap-2 whitespace-nowrap rounded-xl bg-primary px-5 py-3 text-sm font-bold text-primary-foreground transition-transform hover:-translate-y-0.5 sm:gap-3 sm:px-7 sm:py-4 sm:text-base ${className}`"
  >
    Залишити заявку на передзапис
    <span
      class="grid size-7 shrink-0 place-items-center rounded-lg bg-background text-primary transition-transform group-hover:translate-x-0.5 sm:size-8"
    >
      ↘
    </span>
  </a>
</template>
