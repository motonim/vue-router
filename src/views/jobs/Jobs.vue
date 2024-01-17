<template>
    <h1>Jobs</h1>
    <router-link class="job" v-for="job in jobs" :key="job.id" :to="{ name: 'jobDetails', params: { id: job.id }}">
        <h2>{{ job.title }}</h2>
    </router-link>
</template>
<script>
export default {
    data() {
        return {
            jobs: [
                { title: 'UX designer', id: 1, details: 'lorem'},
                { title: 'Web developer', id: 2, details: 'lorem 14123'},
                { title: 'DevOps engineer', id: 3, details: 'lorem ipsum 23234234'},
            ]
        }
    }
}
</script>

<style scoped>
 .job h2{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
  }
  .job h2:hover {
    background: #ddd;
  }
  .job a{
    text-decoration: none;
  }
</style>