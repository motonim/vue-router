<template>
    <h1>Job Details Page</h1>
    <!-- <p>The job id is {{ $route.params.id  }}</p> -->
    <p>The job id is {{ id  }}</p>
    <!-- <p>{{  job.details  }}</p> -->
</template>

<script>
export default {
    props: ['id'], // we don't need data() function anymore because we declared props to be true on index.js
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     }
    // }
}

</script>
