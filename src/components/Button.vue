<script setup>

  defineProps({
   name: String,
   color: {
    type: String,
    default: 'default'
  },
   variant: String,
   disabled: Boolean,
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
    }" :disabled="disabled"> {{name}} </button>
    <div class="right">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>

  button{
    padding: 10px 20px;
    border-radius: 12px;
    border: none;
    font-family: 'Noto Sans JP', sans-serif;
    margin-block-start: 3rem;
  }

  .buttons{
    position: relative;
  }

  .left{
    position: absolute;
    left: 20px;
  }

  .default{
    background-color: #E0E0E0;
    color: #3F3F3F;
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


</style>
