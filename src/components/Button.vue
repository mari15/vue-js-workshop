<template>
   <button v-on:click="msg('hello vue')" :class="{  active: isActive }">{{ text }}</button> 

</template>

<script>
  export default {
    name: 'Button',

    props: {
      text: {
        type: String,
        required: true
      },
      height: {
        type: Number,
        default: 100
      },
      width: {
        type: Number,
        default: 100
      },

      isActive: {
        type: Boolean,
        default: true
      }
    },

    methods: {
      msg: function (message) {
        alert(message)
      }
    }
  }
</script>

<style scoped>
  button {
    font-size: 40px;
    padding: 10px 50px;
    border-radius: 20px;
    background-color: #fff;
    color: #000;
  }

  .active {
    background-color: #000;
    color: #fff;
  }
</style>
