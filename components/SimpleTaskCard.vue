<template>
  <div class="flex items-center gap-3 p-4 rounded-md bg-white shadow-sm">
    <input type="checkbox" class="w-4 h-4 rounded-md" />
    <div>
      <h3 class="text-lg font-medium">{{ title }}</h3>
      <p class="text-gray-500">{{ subtitle }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
};
</script>
