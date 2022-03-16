<template>
  <div class="about">
    <p><button @click="orange = !orange">Apply colour</button></p>
    <p :class="{ orange }">I need some colour bro</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myClass: "orange",
      orange: true,
    };
  },
  methods: {
    change() {
      if (this.myClass === "orange") {
        this.myClass = "blue";
      } else {
        this.myClass = "orange";
      }
    },
  },
};
</script>

<style>
.orange {
  background-color: orange;
}

.blue {
  background-color: blue;
}
</style>
