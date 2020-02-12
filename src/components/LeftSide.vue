<template>
    <div class="row">
        <div>
            <img src="../assets/trompeta.jpg" alt="" class="image">
        </div>
        <div class="buttons">
            <button
                type="button"
                class="knof row btn btn-secondary"
                @click="changeText(about)"
                >About me</button>
            <button
                type="button"
                class="knof row btn btn-secondary"
                @click="changeText(projects)"
                >My projects</button>
            <button
                type="button"
                class="knof row btn btn-secondary"
                @click="changeText(contact)"
                >Contact me</button>
            <button
                type="button"
                class="knof row btn btn-secondary"
                @click="changeText(resume)"
                >Resume</button>
        </div>
    </div>
</template>


<script>
    export default {
        data: () => {
            return {
                textSelect: "hey",
                about: 'appAbout',
                projects: 'appProject',
                contact: 'appContact',
                resume:'appResume',
            }
        },
        methods: {
            changeText(btnName) {
                this.textSelect = btnName;
                this.$emit('componentChange', this.textSelect);
            }
        },
        props: ['currentText']
        
    }
</script>


<style lang="scss">
    .buttons {
        margin: 10% 0% 0% 0%;
    }
    .knof {
        opacity: 0.7;
        margin: 4% 15%;
        width: 70%;

    }
    .image {
        margin: 15% 0% 0% 15%;
        width: 80%;
        border-radius: 50%;
    }
</style>