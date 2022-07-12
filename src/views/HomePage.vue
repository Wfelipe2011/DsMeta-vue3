<script lang="ts" setup>
  import { IProduct } from '~/interface/IProduct';
  const products: IProduct[] = [
    {
      id: 1,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 2,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 3,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 4,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 5,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 6,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 7,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
    {
      id: 8,
      seller: 'Wilson Felipe',
      date: '2020-01-01',
      total: 'R$ 100,00',
      visits: 10,
      sales: 10,
    },
  ];
</script>

<template>
  <div class="">
    <Logo />
    <Box>
      <Title>Vendas</Title>
      <!-- FIltro -->
      <div class="my-6 mb-10 flex flex-col gap-4">
        <input
          class="input"
          type="date"
        />
        <input
          class="input"
          type="date"
        />
      </div>

      <TableSales :products="products" />
    </Box>
  </div>
</template>

<style scoped>
  .input {
    @apply w-full rounded-lg bg-[#1B2531] p-2 px-3 text-gray-400 md:w-[300px];
  }
</style>
