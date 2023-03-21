<template>
  <Button @test-test="changeSpanData" label="Soy una prop" color="red" backgroundColor="white" padding="20px"
    font="small"></Button>
  <span>{{ contador.count }}</span>
  <Button @test-test="changeSpanData" label="Soy una prop" color="blue" backgroundColor="white" padding="20px"
    font="small"></Button>
  <span>{{ contador.doubleCount }}</span>
</template>

<script setup>
import Button from '../components/Button.vue';

import { useCounterStore } from '@/stores/counter';

const contador = useCounterStore();


function changeSpanData(count) {
  console.log(count);
}
</script>
