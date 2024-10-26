<template>
  <div class="absolute w-full top-2 left-0 flex justify-center px-8">
    <div
      class="p-4 bg-white self-start mt-32 max-w-screen-md"
      v-if="modalActive"
    >
      <slot class="" />
      <button
        class="text-white mt-8 bg-primary py-2 px-6"
        @click="$emit('close-modal')"
      >
        Close
      </button>
    </div>
  </div>
</template>

<script setup>
defineEmits(["close-modal"]);
defineProps({
  modalActive: {
    type: Boolean,
    default: false,
  },
});
</script>

<style lang="scss" scoped>
</style>