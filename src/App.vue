<script setup>
import { ref } from "vue";

const counter = ref(0);
</script>

<template>
  <main>
    <div class="container">
      <h1>The current count is...</h1>
      <p>{{ counter }}</p>
      <div>
        <button class="btn" :disabled="counter === 0" @click="counter--">
          -
        </button>
        <button class="btn" :disabled="counter === 20" @click="counter++">
          +
        </button>
      </div>
    </div>
  </main>
</template>

<style scoped>
.container {
  border-radius: 12px;
  padding: 30px;
  background-color: rgb(240, 240, 240);
  min-width: 600px;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.container h1 {
  padding: 0 20px;
  color: rgb(75, 75, 75);
  font-size: 30px;
  font-weight: normal;
}

.container p {
  font-size: 70px;
  padding: 20px;
  font-weight: bold;
  margin: 20px 0;
  color: rgb(75, 75, 75);
}

.container .btn {
  border: none;
  width: 150px;
  padding: 8px 30px;
  text-align: center;
  color: rgb(75, 75, 75);
  margin: 0 20px;
  font-size: 24px;
  border-radius: 50px;
  background-color: rgb(255, 139, 139);
  cursor: pointer;
}

.container .btn:disabled {
  cursor: not-allowed;
  background-color: rgba(255, 139, 139, 0.425);
}
</style>
