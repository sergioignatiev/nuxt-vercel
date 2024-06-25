<template>
  <div class="todo">
    <form @submit.prevent="addTodo">
   <input placeholder="Добавить задачу" type="text" class="input" required v-model="todo">
<button class="todo-submit">добавить</button>   
</form>

<div class="task-wrapper" v-show="list">
   <div class="task" v-for="task in list" :key="task.id" v-show="task.isVisible">
    <h2 class="task-task">{{ task.task }}</h2>
<button class="task-completed" @click="task.completed=true" v-show="task.completed==false">Завершить</button>
<button class="task-completed task-finished" v-show="task.completed">Завершено</button>
<button class="task-completed task-button" @click="task.isVisible=false">Удалить</button>
   </div>
</div>
  </div>
</template>

<script setup>
useHead({
    title:"Todo"
})
const list=ref([])
const todo=ref('')
function addTodo(){
list.value.push({id:list.value.length+1,task:todo.value,completed:false,isVisible:true})
todo.value=''
}
</script>

<style scoped>
.todo {
    margin:20px;
    min-height: 100vh;
    font-family: Arial, Helvetica, sans-serif;
}
.input {
  display: block;
width:100%;
height:40px;
border-radius: 8px;
padding:0px 10px;


}
.todo-submit {
width:100%;
height:40px;
border:none;
background-color: green;
border-radius: 8px;
margin-top: 10px;
font-size: 25px;
text-transform: uppercase;
color:white;
}
.task-wrapper {
    display:flex;
    flex-wrap: wrap;
}
.task {
    width:300px;
    margin:10px;
    display:flex;
    flex-direction: column;

border-radius: 10px;
border: 1px solid blue;
padding: 10px;

}
.task-task {
}
.task-completed {
    padding:10px 20px;
    border-radius: 8px;
    border:none;
    background-color: blue;
    color:white;
    font-weight: 600;
    font-size: 20px;
    margin-top: 20px;
}
.task-finished {
    background-color: rgb(12, 188, 12);
}
.task-button {
    background-color: red;
}
</style>