
<template>
  <div class="bg-gray-100 h-screen">
    
    <div class="bg-gray-100 flex flex-col items-center">
      <h1 class="text-3xl font-bold mt-10">Tarefas</h1>
    </div>
    
    
  
    <div class="bg-gray-100 h-screen  w-screen flex gap-y-4  flex-col items-center">
      
      <div class="w-3/4 flex content-center flex-row  items-center gap-3 p-4 rounded-md bg-white shadow-sm">
        <input v-on:keyup.enter="addTask" v-model="taskTitle" placeholder="new Task" class="w-full text-md font-medium"/>
        <button class="text-2xl font-bold center">+ </button>
      </div>


      <div v-for="task in Tasks" :key="task.title" class="w-3/4 ">
        <SimpleTaskCard :title="task.title" :subtitle="task.subtitle" />
      </div>
    </div>
  </div>

</template>


<script setup lang="ts">
import SimpleTaskCard from '~/components/SimpleTaskCard.vue';
import NewTaskCard from '~/components/NewTaskCard.vue';
const taskTitle = ref("")
var Tasks = [
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

const addTask = ()=>{
  if (taskTitle.value !== ""){
    console.log(taskTitle.value)
    Tasks.push({
      title: taskTitle.value,
      subtitle: ""
    })
    taskTitle.value = ""
  }
}


</script>