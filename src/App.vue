<script setup lang="ts">
import { ref, watch } from 'vue';
import ResultPanel from './components/ResultPanel.vue';
import FansGroup from './components/FansGroup.vue';

const counter = ref(0);
const incrementCounter = () => counter.value++;

const libName = ref(counter.value % 2 ? 'Red' : 'Blue');
watch(counter, (newValue: number) => {
  libName.value = newValue % 2 ? 'Red' : 'Blue';
});
</script>

<template>
  <div
    class="flex justify-between p-2 bg-slate-100 text-black shadow-inner border border-slate-300 border border-slate-300"
  >
    <div>
      <ResultPanel />
      <div>
        <FansGroup name="Red" />
        <FansGroup name="Blue" />
        <br />
        <button class="flex justify-between m-6" @click="incrementCounter">
          Swich away from {{ libName }}
        </button>
        <FansGroup :name="libName" />
      </div>
    </div>
  </div>
</template>
