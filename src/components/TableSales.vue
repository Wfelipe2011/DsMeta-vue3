<script lang="ts" setup>
  import { defineProps } from 'vue';
  import IcNotify from '../assets/img/icons/IcNotify.vue';

  import { PropType } from 'vue';
  import { IProduct } from '~/interface/IProduct';

  const props = defineProps({
    products: {
      type: Array as PropType<IProduct[]>,
      required: true,
    },
  });
</script>
<template>
  <table class="my-6 w-full">
    <tr class="border-b border-gray-400 text-gray-300">
      <th class="hidden lg:table-cell">Id</th>
      <th class="hidden md:table-cell">Data</th>
      <th>Vendedor</th>
      <th class="hidden lg:table-cell">Visitas</th>
      <th class="hidden lg:table-cell">Vendas</th>
      <th>Total</th>
      <th>Notificar</th>
    </tr>
    <tr
      v-for="product in props.products"
      :key="product.id"
      class="border-b border-gray-600 text-gray-300"
    >
      <td class="hidden lg:table-cell">{{ product.id }}</td>
      <td class="hidden md:table-cell">{{ product.date }}</td>
      <td>{{ product.seller }}</td>
      <td class="hidden lg:table-cell">{{ product.visits }}</td>
      <td class="hidden lg:table-cell">{{ product.sales }}</td>
      <td>{{ product.total }}</td>
      <td class="flex justify-center">
        <button class="rounded-md border border-[#FF6B72] p-2 brightness-75 hover:brightness-100">
          <IcNotify />
        </button>
      </td>
    </tr>
    {{}}
  </table>
</template>
<style scoped>
  th {
    @apply py-2;
  }
  td {
    @apply py-4 text-center text-gray-400;
  }
</style>
