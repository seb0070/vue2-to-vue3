<template>
  <div>
    <input v-model="message" />
    <p>{{ message }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// 반응형 변수 정의
const message = ref('Hello Vue')
</script>