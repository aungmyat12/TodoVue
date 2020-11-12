<template>
  <button v-if="showClearCompletedButton" @click="clearCompleted">
    Clear Completed
  </button>
</template>

<script>
    export default {
        name: "TodoClearCompleted",
        props: {
          showClearCompletedButton: {
            type: Boolean,
            required: true
          }
        },
        methods: {
          clearCompleted() {
            eventBus.$emit('clearCompletedTodos')
          }
        }
    }
</script>

<style scoped>

</style>
