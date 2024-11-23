<template>
    <input type="text" v-model="updatedModelValue">
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  modelValue: { type: String, required: true },
})

const emit = defineEmits(['update:modelValue'])

const updatedModelValue = computed({
  get: () => props.modelValue,
  set: (newValue) => emit('update:modelValue', newValue.replace(/\D/g,''))
})

// function addSpaces(str) {
//   const reverset = [...str].reverse()
//   const resultArr = []

//   for (let i = 0; i < reverset.length; i++) {
//     if ((i + 1) % 3 === 0) {
//       resultArr.push(reverset[i], ' ')
//     } else {
//       resultArr.push(reverset[i])
//     }
//   }
//   return resultArr.reverse().join('')
// }

</script>

<style lang="scss" scoped>

</style>