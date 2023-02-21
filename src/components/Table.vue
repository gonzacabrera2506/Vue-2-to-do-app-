<template>
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
                    <input type="checkbox">
                </td>
                <td>
                    {{ task.titulo }}
                </td>
                <td>
                    <button>DELETE</button>
                </td>
            </tr>
        </tbody>
    </table>          
</template>

<script>
    export default {
        name: 'tasks',
        data() {
            return {
                tasks: [
                    {
                        titulo: 'task 1'
                    },
                    {
                        titulo: 'task 2'
                    },
                    {
                        titulo: 'task 3'
                    }
                    
                ]
            }
        }
    }
</script>

<style>
</style>

