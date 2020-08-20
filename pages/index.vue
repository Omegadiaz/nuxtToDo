<template>
  <div class="container">
    <div>
      <h1 class="title">El TODO de {{ newTask }}</h1>
    </div>
    <div>
      <form class="flex flex-wrap">
        <input
          v-model="newTask"
          type="text"
          class="w-full border p-4 bg-gray-200 border rounded my-4"
        />
        <button class="w-full bg-blue-600 rounded p-2 text-white">
          Añadir tarea
        </button>
      </form>
      <div>
        <ul>
          <li>Tarea</li>
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
    }
  },
}
</script>
