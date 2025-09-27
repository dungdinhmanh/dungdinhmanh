<template>
  <span class="iconfont icon-search search" @click="showDialog"></span>
</template>

<script setup lang="ts">
import { useStore } from '../../store'
const { state } = useStore()

const showDialog = () => {
  state.searchDialog = true
  state.showDropdownMenu = false
}
</script>

<style scoped lang="less">
.search {
  cursor: pointer;
  font-size: 1.6rem;
  color: var(--font-color-grey);
  width: 1.8rem;
  height: 1.8rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

@media (max-width: 768px) {
  .search {
    font-size: 1.6rem;
    width: 1.6rem;
    height: 1.6rem;
  }
}
</style>
