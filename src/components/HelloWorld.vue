<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(10)
</script>

<template>
 <div><h1>{{ msg }}</h1>
    <el-button type="button" @click="count++">count is {{ count }}</el-button></div> 
</template>

<style scoped>
a{
  color: #888;
}
</style>
