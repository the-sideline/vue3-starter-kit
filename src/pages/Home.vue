<script setup lang="ts">
import { useCounterStore } from '@/store/counter'
import BaseButton from '@/components/base/BaseButton.vue'
import { useI18n } from 'vue-i18n'

const counter = useCounterStore()
const { t } = useI18n()
</script>

<template>
  <main>
    <h1>{{ t('welcome') }}</h1>
    <div class="counter-demo">
      <h2>{{ t('counter') }}</h2>
      <p>{{ t('hello') }}</p>
      <p>{{ t('counter') }}: {{ counter.count }}</p>
      <p>Double: {{ counter.doubleCount }}</p>
      <BaseButton @click="counter.increment" primary>
        {{ t('increment') }}
      </BaseButton>
    </div>
  </main>
</template>

<style scoped>
.counter-demo {
  text-align: center;
  padding: 2rem;
}

.counter-demo h2 {
  color: #42b983;
  margin-bottom: 1rem;
}

.counter-demo p {
  font-size: 1.2rem;
  margin: 0.5rem 0;
}
</style>
