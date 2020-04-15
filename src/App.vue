<template>
  <div id="app">
    <to-do-form @alteraTexto="adicionaTarefa($event)"/>
    <to-do-list :tarefas="tarefas"/>
  </div>
</template>

<script>
import ToDoForm from "./components/ToDoForm.vue"
import ToDoList from "./components/ToDoList.vue"
export default {
  name: 'App',
  components: {
    ToDoForm,
    ToDoList
  }, data: function(){
    return{
      tarefas:[
        {descricao:"Matemática"},
        {descricao:"Biologia"},
      ]
    }
  },methods:{
    adicionaTarefa:function(event){
      this.tarefas.push({descricao:event.texto})
    },
  }
}
</script>

<style>
</style>
