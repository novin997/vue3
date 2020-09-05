<template>
  <v-carousel cycle heigth="400">
    <v-carousel-item v-for="(slide, i) in state.slides" :key="i"></v-carousel-item>
  </v-carousel>
</template>

<style lang="scss"></style>

<script lang="ts">
import { ref, defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {
    const state = ref<object>({
      slides: ["1", "2", "3", "4", "5"],
    });

    return {state};
  },
});
</script>
