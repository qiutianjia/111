<template>
  <div class="pbody">
    <count
      v-for="item in listInfo"
      v-model="item.shopCount"
      :key="item.id"
    ></count>
  </div>
</template>
<script>
import count from "./components/count.vue";
export default {
  name: "placeAnOrder",
  components: {
    count,
  },
  data() {
    return {
      value: 0,
      listInfo: [{ id: 0, shopCount: 0 }],
    };
  },
};
</script>