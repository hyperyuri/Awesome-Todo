<template>
  <div class="q-mt-lg">
    <listHeader bgColor="bg-green-4">Completed</listHeader>

    <q-list
     bordered
     separator
    >

      <task
       v-for="(task, key) in tasksCompleted"
       :key="key"
       :task="task"
       :id="key"
      ></task>
    </q-list> 
    </div>
</template>

<script>
export default {
  props: ['tasksCompleted'],
  components: {
    task: require('components/Tasks/Task.vue').default,
    listHeader: require('components/Shared/ListHeader.vue').default
  }
}
</script>

<style>

</style>