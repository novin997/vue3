<template>
  <v-carousel hide-delimiters cycle height="600">
    <v-carousel-item
      v-for="(image, i) in state.images"
      :key="i"
    >
      <v-img height="600" :src="image.src" :position="image.position">
        <v-row class="fill-height" align="center" justify="center">
          <div class="display-3 black--text">Hello</div>
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
          src: require("../assets/images/K-On.jpg"),
          position: "top",
        },
        {
          src: require("../assets/images/your-lie-in-april.jpg"),
          position: "top",
        },
        {
          src: require("../assets/images/tokyo-ghoul.jpg"),
          position: "top",
        },
        {
          src: require("../assets/images/your-name.png"),
          position: "bottom",
        },
      ],
    });
    return { state };
  },
});
</script>
