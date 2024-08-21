
<template>
  <div class="bg-gray-100 h-screen">
  <div class="bg-gray-100 flex flex-col items-center">
    <h1 class="text-3xl font-bold mt-10">Tarefas</h1>
  </div>
  <div class="bg-gray-100 h-screen  w-screen flex  items-center">

   <div v-for="task in Tasks" :key="task.title" class="flex flex-col items-center">
    <SimpleTaskCard :title="task.title" :subtitle="task.subtitle" />
   </div>
  </div>
  </div>
</template>

<script lang="ts">
import SimpleTaskCard from '~/components/SimpleTaskCard.vue';

const Tasks = [
  {
    title: "task 1",
    subtitle: "task 2",
  },
  {
    title: "task 1",
    subtitle: "task 2",
  },
  {
    title: "task 1",
    subtitle: "task 2",
  },
]


</script>