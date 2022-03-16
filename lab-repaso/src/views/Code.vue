<template>
  <div>
    <b-row>
      <b-col class="col-10 offset-1">
        <Card v-for="card in cards" :title="card.title" :key="card.id"> </Card>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import Card from "../components/Card.vue";
export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          title: "Card 1",
          content: "Content of card 1",
          soldout: true,
          button: "Button 1",
        },
        {
          id: 2,
          title: "Card 2",
          content: "Content of card 2",
          button: "Buton 2",
        },
        {
          id: 3,
          title: "Card 3",
          content: "Content of card 3",
          button: "Buton 3",
        },
      ],
    };
  },
  components: {
    Card,
  },
};
</script>

<style>
.red {
  background: red;
}

.blue {
  background: blue;
}
</style>
