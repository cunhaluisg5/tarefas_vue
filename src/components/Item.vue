<template>
  <div id="item">
    <ul>
      <li v-for="task in lista" :key="task.key">
        <span>{{task.text}}</span>
        <button @click="deleteItem(task.key)">Concluir</button>
      </li>
    </ul>
  </div>
</template>

<script>
  export default{
    name: 'ItemComponent',
    props:[
      'lista',
      'delete'
    ],
    methods:{
      deleteItem(key){
        this.delete(key)
      }
    }
  }
</script>

<style scoped>
  #item{
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  ul{
    list-style: none;
    padding: 0;
    margin-top: 20px;
  }

  ul li{
    padding: 15px 0;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  li:not(:first-child){
    border-top: 1px solid #EEE;
  }

  span{
    color: #0D2636;
  }

  button{
    cursor: pointer;
    background: #DDD;
    color: #000;
    border: 0;
    padding: 8px 8px;
    outline: none;
    border-radius: 4px;
  }
</style>