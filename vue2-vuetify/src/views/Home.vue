<template>
  <v-carousel hide-delimiters cycle heigth="800">
    <v-carousel-item 
      v-for="(image, i) in state.images" 
      :key="i"
    >
      <v-img :src="image.src">
        <v-row class="fill-height" align="center" justify="center">
          <div class="display-3 white--text">Hello</div>
        </v-row>
      </v-img>
    </v-carousel-item>
  </v-carousel>
</template>

<style lang="scss"></style>

<script lang="ts">
import { ref, defineComponent } from "@vue/composition-api";

declare let require: any;

export default defineComponent({
  setup() {
    const state = ref<object>({
      images: [
        {
          src: require("../assets/K-On.jpg")
        },
      ],
    });
    return {state};
  },
});
</script>
