<template>
    <button 
        v-on:click="$emit('welcome')"
        :class="dark ? 'dark-theme' : 'light-theme'"

    >
        <slot>{{text}}</slot>
    </button>
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

        dark: {
            type: Boolean,
            default: false
        }
    }
  }
</script>

<style lang="scss" scoped>
@import '@/assets/_shared.scss';

    button {
        font-size: 40px;
        padding: 10px 50px;
        border-radius: 20px;
        margin-left: 50px;
    }

    .dark-theme {
        background-color: $black;
        color: $white;
    }

    .light-theme{
        background-color: $white;
        color: $black;
    }
</style>
