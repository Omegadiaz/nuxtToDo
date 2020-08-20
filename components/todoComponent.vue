<template>
  <div>
    <form class="flex flex-wrap" @submit.prevent="addToList()">
      <input
        v-model="externalTask"
        type="text"
        class="w-full border p-4 bg-gray-200 border rounded my-4"
      />
      <button type="submit" class="w-full bg-blue-600 rounded p-2 text-white">
        Añadir tarea
      </button>
    </form>
    <div>
      <div>
        <ul v-for="(task, index) in allTasks" :key="`task-${index}`">
          <li class="my-2">
            <div>
              <input
                v-model="allTasks[index]"
                class="p-4 bg-gray-100 rounded"
                type="text"
              />
              <button
                class="bg-red-500 text-white rounded p-4"
                @click="deleteTask(index)"
              >
                Eliminar
              </button>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      newTask: '',
      allTasks: [],
    }
  },
  methods: {
    addToList() {
      this.allTasks.push(this.newTask)
    },
    deleteTask(index) {
      this.allTasks.splice(index, 1)
    },
  },
}
</script>
