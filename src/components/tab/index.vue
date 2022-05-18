<template>
  <div class="tab-animation">
    <ul>
      <li
        v-for="(tab) in tabList"
        @click="currentTab = tab.key"
        :class="tabClass(tab.key)"
        :key="tab.key">
          {{tab.title}}
      </li>
    </ul>
  </div>
</template>
  
  
<script setup lang='ts'>
import { ref } from 'vue';
import './style.scss';

defineOptions({
  name: 'TabAnimation'
})
const currentTab = ref('LINE');
const tabList = [
  {
    title: 'LINE',
    key: 'LINE'
  },
  {
    title: 'FAMILY SERVICE',
    key: 'SERVICE'
  },
  {
    title: 'FAMILY SERVICE1',
    key: 'SERVICE2'
  },
]
const tabClass = (key: string) => {
  return currentTab.value === key ? 'is-active' : 'default';
}
</script>