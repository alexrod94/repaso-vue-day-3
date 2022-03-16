<template>
  <div>
    <router-link to="/code">Go to code</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  components: {
    Navbar,
  },
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

<style></style>
