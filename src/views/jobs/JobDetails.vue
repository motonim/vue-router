<template>
    <div v-if="job">
        <h1>{{  job.title }}</h1>
        <!-- <p>The job id is {{ $route.params.id  }}</p> -->
        <p>The job id is {{ id  }}</p>
        <p>{{  job.details  }}</p>
    </div>
    <div v-else>
        <p>Loading job details... </p>
    </div>
</template>

<script>
export default {
    props: ['id'], // we don't need data() function anymore because we declared props to be true on index.js
    data() {
        return {
            job: null
        }
    },
    mounted() {
        fetch('http://localhost:3000/jobs/' + this.id) 
            .then(res => res.json())
            .then(data => this.job = data)
            .catch(err => console.log(err.message))
    }
}

</script>
