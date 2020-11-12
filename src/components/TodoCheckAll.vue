<template>
  <div>
    <label
      ><input
        type="checkbox"
        :checked="!anyRemaining"
        @change="allChecked"
      />
      Check All
    </label>
  </div>
</template>

<script>
export default {
  name: "TodoItemsRemaining",
  props: {
    // remaining: {
    //   type: Number,
    //   required: true
    // },
    anyRemaining: {
      type: Boolean,
      required: true
    },
  },
  methods: {
    allChecked() {
      eventBus.$emit('checkAllChanged',this.anyRemaining);
    }
  }
};
</script>

<style scoped></style>
