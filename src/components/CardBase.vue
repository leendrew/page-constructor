<script lang="ts">
import { defineComponent } from 'vue';
import Stack from '@/components/ui/Stack.vue';

export default defineComponent({
  name: 'CardBase',
  components: {
    Stack,
  },
});
</script>

<template>
  <VSheet
    tag="article"
    class="pa-4 card"
    rounded
    outlined
  >
    <Stack
      class="card-inner"
      direction="column"
      :gap="4"
    >
      <slot />
    </Stack>
  </VSheet>
</template>

<style scoped>
.card {
  position: relative;
}

.card-inner {
  height: 100%;
}
</style>
