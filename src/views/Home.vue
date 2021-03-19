<template>
  <div class="home">
    <v-list
      flat
      class="pt-0"
    >
      <div v-for="task in tasks" :key="task.id">
        <v-list-item-group multiple>
        <v-list-item
        @click="doneTask(task.id)"
        >
          <template>
            <v-list-item-action>
              <v-checkbox :input-value="task.done" color="primary"></v-checkbox>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>{{ task.title }}</v-list-item-title>
            </v-list-item-content>
          </template>
        </v-list-item>
        <v-divider></v-divider>
      </v-list-item-group>
      </div>
    </v-list>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data: () => ({
    tasks: [
      {
        id: 1,
        title: 'Levantar',
        done: true
      }
    ]
  }),
  methods : {
    doneTask(id) {
      let task = this.tasks.filter(task => task.id === id)[0]
      task.done = !task.done
    }
  }
}
</script>
