<template>
  <div>
    <button
      v-for="element in groceries"
      :key="element.id"
      @click="showName(element)"
    >
      {{ element.name }}
    </button>
    <div class="card" :style="{ background: bcgColor }">Esta es mi card</div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  data() {
    return {
      eliodoro: false,
      bcgColor: "#333",
      groceries: [
        { id: 1, name: "Rojo", color: "red" },
        { id: 2, name: "Verde", color: "green" },
      ],
    };
  },
  methods: {
    showName(element) {
      this.bcgColor = element.color;
    },
  },
};
</script>

<style>
.card {
  border: 1px solid black;
  padding: 15px;
  border-radius: 5px;
  color: white;
}
</style>
