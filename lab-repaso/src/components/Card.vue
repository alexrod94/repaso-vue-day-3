<template>
  <div :class="myClass">
    <h2>{{ title }}</h2>
    <Button @myEvent="log" @secondEvent="seeParam" @cambioDeColor="change" />
  </div>
</template>

<script>
import Button from "./Button.vue";
export default {
  data() {
    return {
      myClass: "card",
    };
  },
  props: {
    title: {
      type: String,
    },
    content: {
      type: String,
      default: "Mi contenido",
    },
    button: {
      type: String,
      default: "Este es mi botón por defecto",
    },
  },
  components: {
    Button,
  },
  methods: {
    log() {
      console.log("I'm in my event");
    },
    change() {
      this.myClass = "card-dark";
    },
    seeParam(a) {
      console.log("Este es mi parámetro: " + a.info);
    },
  },
};
</script>

<style>
.card {
  background-color: #f4f4f4;
  padding: 15px;
  border: 1px solid black;
  border-radius: 5px;
}

.card-dark {
  background-color: #333 !important;
  padding: 15px;
  border: 1px solid black;
  border-radius: 5px;
}
</style>
