<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id">
        <h2>{{ job.title }}</h2>
    </div>
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