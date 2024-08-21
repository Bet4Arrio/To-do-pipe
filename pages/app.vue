
<template>
  <div class="bg-gray-100 h-screen">
    <div class="bg-gray-100 flex flex-col items-center">
      <h1 class="text-3xl font-bold mt-10">Tarefas</h1>
    </div>
    
    
  
    <div class="bg-gray-100 h-screen  w-screen flex gap-y-4  flex-col items-center">
      <button class="w-3/4 flex content-center flex-row  items-center gap-3 p-4 rounded-md bg-white shadow-sm">
        <span class="text-2xl font-bold center">+ </span>
      </button>


      <div v-for="task in Tasks" :key="task.title" class="w-3/4 ">
        <SimpleTaskCard :title="task.title" :subtitle="task.subtitle" />
      </div>
    </div>
  </div>

</template>

<script setup lang="ts">
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