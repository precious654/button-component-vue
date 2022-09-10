<script setup>

  defineProps({
   name: String,
   color: {
   type: String,
   default: "default"
   }
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
      'default': color === 'default'
    }"> {{name}} </button>
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


</style>
