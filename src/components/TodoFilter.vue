<template>
  <div>
    <button :class="{ active: filter == 'all' }" @click="changedFilter('all')">
      All
    </button>
    <button
      :class="{ active: filter == 'active' }"
      @click="changedFilter('active')"
    >
      Active
    </button>
    <button
      :class="{ active: filter == 'completed' }"
      @click="changedFilter('completed')"
    >
      Completed
    </button>
  </div>
</template>

<script>
export default {
  name: "TodoFilter",
  data() {
    return {
      filter : 'all'
    }
  },
  methods: {
    changedFilter(filter) {
      eventBus.$emit('filterChanged',filter);
    }
  }
};
</script>

<style scoped></style>
