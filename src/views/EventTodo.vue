<!-- (24-02-01-thu) -->

<template>
  <div>
    <input type="text" v-model="todo" />
    <button @click="addTodo">추가</button>
  </div>
  <div>
    <ul>
      <li v-for="todo in todoList" v-bind:key="todo.no">
        {{ todo.no + " / " + todo.text }}
        {{ `${todo.no} - ${ todo.text}` }}
        <button v-on:click="deleteTodo(todo.no)">삭제</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todo: "다음할일", //{ no: 3, text: "다음할일" }, //공란을 기준으로 구분.
      todoList: [
        { no: 1, text: "할일1" },
        { no: 2, text: "할일2" },
      ],
    };
  },
  methods: {
    addTodo() {
      let no, text;
      no = this.todoList[this.todoList.length - 1].no + 1;
      text = this.todo;
      this.todoList.splice(no - 1, 0, { no, text });
      this.todo = "";
    },
    deleteTodo(no){
      console.log('no:', no)
      this.todoList = this.todoList.filter(todo => todo.no == no ? false : true) // filter : true만 새로운 값에 담아줌

    }
  },
};
</script>
