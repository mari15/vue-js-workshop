<template>
   <Button text="Click me"/>
</template>

<script>
// @ is an alias to /src
import Button from "@/components/Button.vue";

export default {
  name: "Home",
  components: {
    Button,
  },
};
</script>