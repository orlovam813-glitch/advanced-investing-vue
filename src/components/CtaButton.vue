<script setup lang="ts">
withDefaults(defineProps<{ className?: string }>(), {
  className: "",
});
</script>

<template>
  <a
    href="#forma"
    :class="`group inline-flex items-center gap-3 rounded-xl bg-primary px-7 py-4 text-base font-bold text-primary-foreground transition-transform hover:-translate-y-0.5 ${className}`"
  >
    Залишити заявку на передзапис
    <span
      class="grid size-8 place-items-center rounded-lg bg-background text-primary transition-transform group-hover:translate-x-0.5"
    >
      ↘
    </span>
  </a>
</template>
