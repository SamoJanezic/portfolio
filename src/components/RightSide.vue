<template>
    <div class="text-box">
        <component :is="component"></component>
    </div>
</template>


<script>
    import about from './RTemplates/about.vue';
    import project from './RTemplates/projects';
    import contact from './RTemplates/contact';
    import resume from './RTemplates/resume';

    export default {
        components: {
            appAbout: about,
            appContact: contact,
            appProject: project,
            appResume: resume,
        },
        data: () => {
            return {
                data: {
                }
            }
        },
        methods: {

        },
        props: ['component'],
    }
</script>


<style scoped>
    .text-box {
        /* background-color: rgba(0,0,0,0.25); */
        margin: 7% 10% 0% 10%;
        height: 80%;
        text-align: center;
    }
</style>