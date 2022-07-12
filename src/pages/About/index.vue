<template>
  <div class="container mt-10 flex flex-col items-center justify-center space-y-10">
    <span class="text-4xl">{{ count }}</span>
    <span>{{ countLimit }}</span>
    <div class="flex gap-2">
      <button
        class="rounded bg-primary-600 py-2 px-6 text-white"
        @click="increment"
      >
        Incrementar
      </button>
      <button
        class="rounded bg-primary-600 py-2 px-6 text-white"
        @click="decrement"
      >
        Decrementar
      </button>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        count: 0,
      };
    },
    methods: {
      increment() {
        this.count += 1;
      },
      decrement() {
        if (this.count === 0) return;
        this.count -= 1;
      },
    },
  };
</script>
