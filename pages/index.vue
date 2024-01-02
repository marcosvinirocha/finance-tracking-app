<template>
  <section class="flex items-center justify-between mb-10">
    <h1 class="text-4xl font-extrabold">
      Summary
    </h1>
    <div>
      <USelectMenu :options="transactionView" v-model="viewSelect" />
    </div>
  </section>
  <section class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 sm:gap-16 mb-10">
    <Trend color="green" title="Income" :amount="3000" :last-amount="4000" :loading="false" />
    <Trend color="red" title="Expense" :amount="5000" :last-amount="4000" :loading="false" />
    <Trend color="green" title="Investments" :amount="3000" :last-amount="4000" :loading="false" />
    <Trend color="red" title="Savings" :amount="4000" :last-amount="4000" :loading="false" />
  </section>
</template>

<script lang="ts" setup>
import { transactionView } from '../constants';


const viewSelect = ref(transactionView[1])
</script>

<style></style>