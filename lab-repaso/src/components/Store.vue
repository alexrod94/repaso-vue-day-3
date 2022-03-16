<template>
  <div>
    <b-button variant="danger" @click="callEvent">{{ title }}</b-button>
    <b-button variant="primary" @click="$emit('secondEvent', 2)"
      >Second button</b-button
    >
    <b-button variant="secondary" @click="addOne">Third button</b-button>
  </div>
</template>

<script>
import { useStore } from "../stores/counterStore";
export default {
  setup() {
    const counterStore = useStore();
    return { counterStore };
  },
  props: {
    title: {
      type: String,
      default: "Click here",
    },
  },
  methods: {
    callEvent() {
      this.$emit("myEvent");
    },
    addOne() {
      console.log(this.counterStore.name);
    },
  },
};
</script>

<style></style>
