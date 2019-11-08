<template>
  <div>
    <form v-on:submit.prevent="submitForm">
      <div class="form__item">
        <label for="name">Todo List</label>
        <input type="name" name="todoApp" id v-model="newTask.task" />
      </div>
      <button type="submit">Add More</button>
      <p>Total task {{total}}</p>
      <p>Dleted items {{itemsDeleted}}</p>

    </form>
    <table>
      <thead>
        <tr>
          <th>Todo</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(todo, index) in todos" v-bind:key="index">
          <td>{{todo.task}}</td>
          <td>
            <button v-on:click="deleteButton(index)" class="delete-btn">x</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  name: "TodoApp",
  data() {
    return {
      newTask: {
        task: ""
      },
      todos: [],
      itemsDeleted:0
    };
  },
  methods: {
    submitForm() {
      this.todos.push(this.newTask);
      this.clearForm();
    },
    deleteButton(index) {
      this.todos.splice(index, 1);
      this.itemsDeleted = this.itemsDeleted + 1;
    },
    clearForm() {
      this.newTask = {
        task: ""
      };
    }
  },

  computed: {
   total() {
     return this.todos.length
   }
  }

};
</script>