<template>
  <div class="container">
    <div>
      <h1 class="title">El TODO de {{ newTask }}</h1>
    </div>
    <div>
      <form>
        <input
          v-model="newTask"
          type="text"
          class="border bg-green p-4 bg-green-500"
        />
        <button></button>
      </form>
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
