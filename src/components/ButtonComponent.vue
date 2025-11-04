<script setup lang="ts">
import { ref } from 'vue';

const buttonText = ref('Button not clicked');

function handleClick() {
  buttonText.value = 'Button clicked';
}
</script>

<!-- Component template Button -->
<template>
  <div id = "button-component">
    <button @click="handleClick">Button</button>
  </div>
</template>

<style>
#button-component {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  

}

</style>