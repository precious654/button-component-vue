<script setup>
  import Button from "./components/Button.vue"
</script>

<template>
  <div class="app">

    <div class='bottom-buttons'>
      <Button name="Default" color="default" />
      <Button name="Secondary" color="secondary" />
      <Button name="Danger" color="danger" />
      <Button name="Primary" color="primary" />
    </div>
  </div>
</template>

<style scoped>

  .app{
    inline-size: 80%;
    margin: auto;
  }

  .bottom-buttons{
    display: flex;
    justify-content: space-between;
  }
</style>
