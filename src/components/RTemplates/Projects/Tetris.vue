<template>
    <div>
        <div class="row">
            <img src="../../../assets/Screenshot-tetris.png" class="img col-5">
            <div class="title text col-7">
                <h1>Tetris-v3</h1>
                <div>
                    JavaScript, HTML, CSS
                </div>
                <div class="desc">
                    <p>This is a simple tetris clone. It was my first project so it still has some bugs left that need squashing.</p>
                    <p>This project has tought me a lot about coding. What to do and more importantly what not to do.</p>
                </div>

            </div>
        </div>
        <div>
            <button
                type="button"
                class="btn btn-primary"
                @click="launchTetris"
            >Demo</button>
            <button
                type="button"
                class="btn btn-primary"
                @click="openGitHubTet"
            >Code</button>
            <button
                type="button"
                class="btn btn-primary"
                @click="goBack"
            >back</button>
        </div>
    </div>
</template>


<script>
    export default {
        data: () => {
            return {
                show: true,
            }
        },
        methods: {
            launchTetris() {
                window.open("http://167.172.98.227/tetris");
            },
            openGitHubTet() {
                window.open("https://github.com/SamoJanezic/Tetris-v3");
            },
            goBack() {
                this.$emit('wentBack');
            }
        }
    }
</script>


<style scoped lang="scss">
    .title {
        
    }
    .text {
        color: rgba(255, 255, 255, 0.70);
        text-align: center;
    }
    .tools{
        text-align: center;
    }
    .desc{
        margin: 30px
    }
</style>