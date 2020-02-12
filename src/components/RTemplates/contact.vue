<template>
    <div>
        <h1 class="contact title">Contact me</h1>
        <div class="row">
            <div class="col-6 text">
                <img
                src="../../assets/email-icon.png"
                class="image"
                @click="openMail"
                title="e-Mail me"
                >
            </div>
            <div class="col-6 text">
                <img
                src="../../assets/github-icon.png"
                class="image"
                @click="openGitHub"
                title="Open my GitHub account"
                >
            </div>
            <!-- <a href="mailto:janezic.orion@gmail.com">send mail</a> -->
        </div>
    </div>
</template>


<script>
    export default {
        data: () => {
            return {
                email: 'email',
                github: 'github',
                resume: 'resume',
            }
        },
        methods: {
            openMail() {
                window.open("mailto:janezic.orion@gmail.com");
            },
            openGitHub() {
                window.open("https://github.com/SamoJanezic");
            }
        }
    }
</script>


<style scoped lang="scss">
    .title {
        padding: 6% 0 3% 0;
        color:rgba(255, 255, 255, 0.678);
    }
    .text {
        color: rgba(255, 255, 255, 0.70);
        padding: 0% 10%;
    }
    .image {
        width: 80%;
        cursor: pointer;
    }
</style>