<script>
export default {
  data() {
    return {
      name: 'sam foshati',
      status: 'active',
      tasks: ['task one', 'task two', 'task three'],
      link: 'https://google.com'
    }
  }
}
</script>

<template>
  <p>{{ name }}</p>

  <p v-if="status === 'active'">user is active</p>
  <p v-else-if="status === 'pending'">user is pending</p>
  <p v-else>user is inactive</p>

  <h3>tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <a v-bind:href="link">click for Google</a>
  <a :href="link">click for Google2</a>
</template>
