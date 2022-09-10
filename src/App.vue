<script setup>
  import Button from "./components/Button.vue";
  import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="app">
    <Button name="Default" color="default" />
    <Button name="Default" variant="outline" color="blue" />
    <Button name="Default" variant="text" color="blue" />
    <Button name="Default" disabled='true' />
    <Button name="Default" disabled='true' variant='text'/>

    <div class='bottom-buttons'>
      <Button name="Default" color="default" />
      <Button name="Secondary" color="secondary" />
      <Button name="Danger" color="danger" />
      <Button name="Primary" color="primary" />
    </div>
    <Footer />
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
