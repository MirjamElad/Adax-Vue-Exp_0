<script setup lang="ts">
import { ref, watch } from 'vue';
import ResultPanel from './components/ResultPanel.vue';
import FansGroup from './components/FansGroup.vue';

const duplicateGroupName = ref('Red');
const setDuplicateGroupName = (name) => duplicateGroupName.value = name;

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
        <span class="px-6">Duplicated FANS area:</span>
        <div class="flex px-6 w-18 mt-2">
          <label class="radio-button">
            <input type="radio" checked name="options" value="Red" @click="setDuplicateGroupName('Red')" />
            Red
          </label>
          <label class="radio-button ml-6">
            <input type="radio" name="options" value="Blue" @click="setDuplicateGroupName('Blue')" />
            Blue
          </label>
        </div>
        <FansGroup :name="duplicateGroupName" />
      </div>
    </div>
  </div>
</template>
