<template>
  <div>
    <button @click="add">test</button>
    <div>{{ state.data }}</div>
    <div v-for="item in state.data" :key="item" class="item">
      {{ item.id }}
    </div>
    <Card />
  </div>
</template>

<script lang="ts">
import { reactive, onMounted } from "vue";
import axios from "axios";
import Card from "../components/Card.vue";

export default {
  components: {
    Card
  },
  setup() {
    const state = reactive({
      count: 0,
      data: []
    });

    function add() {
      state.count++;
    }

    async function getData() {
      const res = await axios.get("https://jsonplaceholder.typicode.com/users");
      state.data = res.data;
    }

    onMounted(() => {
      getData();
    });

    return {
      state,
      add
    };
  }
};
</script>

<style lang="scss">
button {
  margin: 5px;
}
</style>
