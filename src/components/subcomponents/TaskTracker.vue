<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
        props: {
            tasks: Object,
            idx: Number
        },
        emits: [
            "removeTaks"
        ]
        methods: {
            done(index) {
                // Emit event to parent to remove task at given index
                this.$emit('remove-task', index)
            }   
        }
    }
</script>

<template>
<!-- TODO: add your template code here --> 
  <div>
    <div class="card mb-3" style="width: 18rem;">
      <div class="card-body">
        <div>
          <h5 class="card-title">Deadline: {{ task.deadline }}</h5>
          <hr>
          <p class="card-text">Description: {{ task.desc }}</p>
        </div>
        <button class="btn btn-success" @click="$emit('removeTask', idx)">Done</button>
      </div>
    </div>
  </div>
</template>