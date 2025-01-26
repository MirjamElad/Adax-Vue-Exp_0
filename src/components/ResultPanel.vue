<script setup lang="ts">
import { defineProps, reactive, ref } from 'vue';
import { getResult } from '../state';
import { useSync } from 'adax-vue';

const data = useSync(()=>[getResult]);
</script>
<template>
  <div
    class="bg-white rounded-xl shadow-lg mx-6 px-6 py-4 border-slate-300 my-2"
  >
    <div class="p-2 text-3xl">
      {{ data?.winnerName }}: ({{ data?.winnerScore }})
    </div>
    <div class="p-2 text-3xl">
      {{ data?.runnerUpName }}: ({{ data?.runnerUpScore }})
    </div>
  </div>
</template>
