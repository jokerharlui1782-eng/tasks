<template>
  <div>
    
    <h1>Ежедневные задания </h1>

    <div class="products">
      <TaskItem 
        v-for="task in tasks" 
        :key="task._id"  
        :task="task"
       >
        
    </TaskItem>
    </div>

  
  </div>
</template>


<script setup lang="ts">
import { ref, computed } from "vue";
import TaskItem from "./components/TaskItem.vue";

const tasks = [
  { _id: "1", title: "Завтрак", text: "Приготовить завтрак и поесть" },
  { _id: "2", title: "пробежка", text: "после завтракак пойти на пробежку" },
  { _id: "3", title: "учёба", text: "пойти на пары" },
  { _id: "4", title: "пойти на работу", text: "после пар идити на работу" },
  { _id: "5", title: "Ужин", text: "Приготовить ужин и поесть" },
  { _id: "6", title: "спать", text: "Приготовиться ко сну" },
];



</script>

<style>
.products {
  display: flex;
  gap: 13px;
  flex-direction: column;
}
</style>

