<script setup lang="ts">
const props = defineProps({
  text: {
    type: String,
    default: '按钮'
  }
})

const emit = defineEmits(['change-text'])

const handleClick = () => {
  emit('change-text', '按钮点击了')
}
</script>
<template>
  <el-button @click="handleClick">{{ text }}</el-button>
</template>