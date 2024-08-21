<template>

<div class="w-3/4 flex content-center flex-row  items-center gap-3 p-4 rounded-md bg-white shadow-sm">
        <input v-on:keyup.enter="addTask" placeholder="new Task" class="w-full text-md font-medium"/>
        <button v-on:click="addTask" class="text-2xl font-bold center">+ </button>
    </div>
</template>

<script setup lang="ts">
interface Props {
  callback: () => void
}

const props = defineProps<Props>()

const addTask = () =>{
   callback("Testet")
}

</script>