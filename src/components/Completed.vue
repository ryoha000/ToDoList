<template>
  <div>
      <div>Completed</div>
      <div v-for="item in items" :key="item.name">
          <div class="item">
              <div class="name">やったこと:{{ item.name }}</div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: "Completed",
  data() {
    return {
      items: [{ name: "書評" }, { name: "掃除" }],
      newItemName: "",
    };
  },
  methods: {
    addItem() {
      this.items.push({ name: this.newItemName, price: this.newItemPrice });
    }
  }
};
</script>

<style>
</style>


