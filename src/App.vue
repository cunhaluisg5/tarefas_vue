<template>
  <div id="app">
    <header>Minhas Tarefas</header>
    <TaskComponent/>
  </div>
</template>

<script>
import TaskComponent from './components/Task.vue';
export default {
  name: 'App',
  components:{
    TaskComponent
  }
}
</script>

<style scoped>
  header{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 80px;
    font-size: 40px;
    color: #FFF;
  }
</style>
