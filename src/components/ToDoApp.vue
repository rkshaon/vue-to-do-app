<template>
  <div class="container">
    <!-- title -->
    <h2 class="text-center mt-5">To Do App with Vue</h2>
    <!-- input -->
    <div class="d-flex">
      <input type="text" placeholder="Enter a to do task..." class="form-control">
      <button class="btn btn-warning rounded-0">Sumibt</button>
    </div>
    <!-- task list table -->
    <table class="table table-bordered">
      <thead>
        <tr>
          <th scope="col">Task</th>
          <th scope="col">Status</th>
          <th scope="col" class="text-center">#</th>
          <th scope="col" class="text-center">#</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(task, index) in tasks" :key="index">
          <td>{{task.name}}</td>
          <td>{{task.status}}</td>
          <td>
            <div class="text-center">
              <span class="fa fa-pen"></span>
            </div>
          </td>
          <td>
            <div class="text-center">
              <span class="fa fa-trash"></span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      tasks: [
        {
          name: 'Hello',
          status: 'to-do'
        },
        {
          name: 'buy something for Bhabi',
          status: 'to-do'
        },
        {
          name: 'git-post-new-repo',
          status: 'to-do',
        },
        {
          name: 'post-on-linked-in',
          status: 'to-do'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
