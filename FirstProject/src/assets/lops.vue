<script>
export default {
  data() {
    return {
      show: true,
      list: [1, 2, 3],
    };
  },
};
</script>
<template>
  <div class="card blue">
    <button @click="show = !show">Toggle List</button>
    <button @click="list.push(list.length + 1)">Push Number</button>
    <button @click="list.pop()">Pop Number</button>
    <button @click="list.reverse()">Reverse List</button>
    <p v-if="list.length === 5">list don't must be 5</p>
    <ul v-else-if="show && list.length">
      <li v-for="item of list">{{ item }}</li>
    </ul>
    <p v-else-if="list.length">List is not empty, but hidden.</p>
    <p v-else>List is empty.</p>
  </div>
</template>