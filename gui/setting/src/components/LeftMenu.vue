<script setup>
import { h } from 'vue'
import { NMenu } from "naive-ui"
import { RouterLink } from 'vue-router'

const menuOptions = [
  {
    label: () => h(RouterLink, {to: {name: 'list'}}, { default: () => '站点管理' }),
    key: 'list',
  },
  {
    label: () => h(RouterLink, {to: {name: 'group'}}, { default: () => '站点分组' }),
    key: 'group',
  },
  {
    label: () => h(RouterLink, {to: {name: 'display'}}, { default: () => '站点排序' }),
    key: 'display',
  },
  {
    label: () => h(RouterLink, {to: {name: 'shortcut'}}, { default: () => '改快捷键' }),
    key: 'shortcut',
  },
  {
    label: () => h(RouterLink, {to: {name: 'set'}}, { default: () => '通用设置' }),
    key: 'set',
  },
  {
    label: () => h(RouterLink, {to: {name: 'feedback'}}, { default: () => '使用反馈' }),
    key: 'feedback',
  }

]
function handleUpdateValue(key, item){
  // console.log('update value', key, item)
}

</script>

<template>
  <n-menu :options="menuOptions" @update:value="handleUpdateValue" />
</template>

<style scoped>

</style>