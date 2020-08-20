<template>
  <div class="container">
    <todo-component :external-task="parentTask" />
    <div>
      <h1 class="title">El TODO de Gabri</h1>
    </div>
    <input class="bg-green-300" v-model="parentTask" type="text" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      parentTask: '',
    }
  },
}
</script>
