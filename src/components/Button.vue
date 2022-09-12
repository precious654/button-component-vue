<script setup>

  defineProps({
   name: String,
   color: String,
   variant: String,
   disabled: Boolean,
   size: String
  })

</script>

<template>
  <div class="buttons">
    <div class="left" v-if="$slots.left">
      <slot name="left"></slot>
    </div>
    <button :class="{
     'secondary': color === 'secondary',
      'primary': color === 'primary',
      'danger': color === 'danger',
      'default': color === 'default',
      'blue': color === 'blue',
      'outline': variant === 'outline',
      'text': variant === 'text',
      'sm': size === 'sm',
      'md': size === 'md',
      'lg': size === 'lg'
    }" :disabled="disabled"> {{name}} </button>
    <div class="right" v-if="$slots.right">
      <slot name="right"></slot>
    </div>
  </div>
</template>

<style scoped>

  button{
    inline-size: 105px;
    padding: 10px 0;
    border-radius: 12px;
    background-color: #E0E0E0;
    color: #3F3F3F;
    border: none;
    font-family: 'Noto Sans JP', sans-serif;
    margin-block-end: 5rem;
  }

  .buttons{
    position: relative;
  }

  .left{
    position: absolute;
    left: 7px;
    bottom: 6px;
    padding-inline-end: 10px;
  }

  .right{
    position: absolute;
    right: 5px;
    bottom: 5px;
    padding-inline-start: 10px;
  }

  .default{
    background-color: #E0E0E0;
    color: #3F3F3F;
  }

  .default:hover{
    background-color: #AEAEAE;
  }

  .secondary{
    background-color: #455A64;
    color: #FFFFFF;
  }

  .secondary:hover{
    background-color: #1C313A;
  }

  .primary{
    background-color: #2962FF;
    color: #FFFFFF;
  }

  .primary:hover{
    background-color: #0039CB;
  }

  .danger{
    background-color: #D32F2F;
    color: #FFFFFF;
  }

  .danger:hover{
    background-color: #9A0007;
  }

  .blue{
    color: #3D5AFE;
  }

  .blue:hover{
    background-color: rgba(41, 98, 255, 0.1);
  }

  .outline{
    border: 1px solid #3D5AFE;
  }

  .text{
    background-color: inherit;
    border: none;
  }

  button:disabled{
    color: #9E9E9E;
  }

  .sm{
    inline-size: 73px;
  }

  .md{
    inline-size: 81px;
  }

  .lg{
    inline-size: 93px;
  }


</style>
