<template>
  <div>
    <b-button variant="danger" @click="callEvent">{{ title }}</b-button>
    <b-button
      variant="primary"
      @click="$emit('secondEvent', { info: 'my info', num: 3 })"
      >Second button</b-button
    >
    <b-button @click="$emit('cambioDeColor')">Cambio color</b-button>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "Click here",
    },
  },
  methods: {
    changeColor() {
      this.$emit("cambioDeColor");
    },
    callEvent() {
      this.$emit("myEvent");
    },
    showAlert() {
      alert("hola");
    },
  },
};
</script>

<style></style>
