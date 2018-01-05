<template>
    <div class="contact-info">
        <h1>{{ name }}</h1>
        <h2>{{ title }}</h2>
        <hr/>
        
    </div>
</template>

<script>
export default {
    name: 'contact-info',
    data () {
        return {
            name: 'Karen Guo',
            title: 'Full Stack Software Developer',
            location: 'Vancouver, BC',

        }
    }
}
</script>

<style scoped>

</style>