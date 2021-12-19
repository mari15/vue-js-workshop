<template>
  <div>
    <Button dark v-on:welcome="sayHi('Hello from the dark side')"> 
      <font-awesome-icon icon="star" /> White star 
    </Button>
    <Button v-on:welcome="sayHi('Hello from light side')">
      Dark star<font-awesome-icon icon="star" />
    </Button>

    <div class='description-wrapper'>
      <h1>Project Description</h1>
      <p>This is a simple VueJs project.</p>
      <p>Home page has two buttons, one button with a dark theme and one button with light theme.</p>
      <p>List page it's a bit more complex, it contains a list of card items with diffent actions on them.</p>
      <p>Check List page for more content!</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Button from "@/components/Button.vue";

export default {
  name: "Home",
  components: {
    Button,
  },

  methods: {
    sayHi: function (msg) {
      alert(msg)
    }
  }
};
</script>

<style lang="scss" scoped>
@import '@/assets/_shared.scss';

  .description-wrapper{
    padding: 20px;
    background-color: $lightGreenBackground;
    width: 80%;
    margin: 50px auto;
  }
</style>