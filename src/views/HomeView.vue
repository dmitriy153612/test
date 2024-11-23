<template>
  <div>
    <app-input v-model="input"/>
    {{ input }}
  </div>
</template>

<script setup>
import AppInput from '@/components/AppInput.vue';
import { ref } from 'vue';

const input = ref('')

</script>

<style lang="scss" scoped>

</style>