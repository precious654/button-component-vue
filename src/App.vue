<script setup>
  import Button from "./components/Button.vue";
  import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="app">
    <Button name="Default" color='default' />
    <Button name="Default" variant="outline" color="blue" />
    <Button name="Default" variant="text" color="blue" />
    <Button name="Default" :disabled=true />
    <Button name="Default" :disabled=true variant='text'/>

    <div class="flex-buttons">
      <Button name="Default" color="primary">
        <template #left>
          <img src="./assets/shoppingcart.svg" alt="icon" width="18" />
        </template>
      </Button>

      <Button name="Default" color="primary">
        <template #right>
          <img src="./assets/shoppingcart.svg" alt="icon" width="18" />
        </template>
      </Button>
    </div>

    <div class="flex-buttons-two">
      <Button name="Default" size="sm" color="primary" />
      <Button name="Default" size="md" color="primary" />
      <Button name="Default" size="lg" color="primary" />
    </div>

    <div class='bottom-buttons'>
      <Button name="Default" color="default" />
      <Button name="Default" color="primary" />
      <Button name="Secondary" color="secondary" />
      <Button name="Danger" color="danger" />
    </div>

    <Footer />
  </div>
</template>

<style scoped>

  .app{
    inline-size: 80%;
    margin: auto;
    padding-block-start: 1rem;
  }

  @media( min-width: 786px) {

    .bottom-buttons{
      display: flex;
      justify-content: space-between;
    }

    .flex-buttons{
      display: flex;
      gap: 16rem;
    }

    .flex-buttons-two{
      display: flex;
      gap: 18rem;
    }

  }


</style>
