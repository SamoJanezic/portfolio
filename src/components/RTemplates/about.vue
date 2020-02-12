<template>
    <div>
        <h1 class="about title">About me</h1>
        <div class="about text">
            {{ aboutMe }}
        </div>
    </div>
</template>


<script>
    export default {
        data: () => {
            return {
                aboutMe: `Aside from working full-time, i've found the time to become a self-tought web developer. From my first hello world to my latest full-stack app i've never grown tired or bored of programming and strive to learn something new everyday.`,
            }
        },
        methods: {
            
        }
    }
</script>


<style scoped>
    .title {
        padding: 6% 0 3% 0;
        color:rgba(255, 255, 255, 0.678);
    }
    .text {
        color: rgba(255, 255, 255, 0.70);
        padding: 0% 10%;
    }
</style>