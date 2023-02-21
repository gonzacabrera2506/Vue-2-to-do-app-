<template>
    <div>
        <table class="table">
            <thead>
                <tr>
                    <th>Checkmark Done</th>
                    <th>Task Name</th>
                    <th>Delete</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="task in tasks">
                    <td>
                        <input type="checkbox" v-model="task.done">
                    </td>
                    <td>
                        {{ task.title }}
                    </td>
                    <td>
                        <button v-on:click="deleteTask(task)" class="btn btn-danger">DELETE</button>
                    </td>
                </tr>
            </tbody>
        </table>
        <!-- Form -->
        <div class="panel panel-default">
            <h2 class="text-center">Add a new task</h2>
            <form v-on:submit="addTask" class="app-form">
                <input type="text" class="form-control" v-model="tasks.title">
                <input type="submit" value="Add" class="btn btn-block btn-primary">
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: 'tasks',
    data() {
        return {
            tasks: [
                {
                    title: 'task 1',
                    done: true
                },
                {
                    title: 'task 2',
                    done: false
                },
                {
                    title: 'task 3',
                    done: false
                }

            ]
        }
    },
    methods: {
        addTask: function (e) {
            e.preventDefault();
            this.tasks.push({
              title: this.tasks.title,
              done: false
            });
          this.tasks.title = '';
          },
        deleteTask: function (task) {
            this.tasks.splice(
                this.tasks.indexOf(task),
                1
            )
        }
    }
}
</script>

<style>
table {
    text-align: center;
}
h2 {
    color: rgb(212, 9, 9);
    }
</style>

