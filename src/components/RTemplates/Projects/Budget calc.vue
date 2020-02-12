<template>
    <div>
        <div class="row">
            <img src="../../../assets/Screenshot-budget_calc.png" class="img col-5">
            <div class="title text col-7">
                <h1>Budget Calculator</h1>
                <div>
                    Javascript, Vue, Laravel, PHP, PostgreSQL
                </div>
                <div class="desc">
                    <p>This is my latest project. It's a budget calculator.</p>
                    <p>It uses Vue for front-end and laravel for backend with postgreSQL serving as a database.</p>
                    <p>It was my first full-stack app, which tought me a lot about creating my own APIs, connecting with databases and using API calls.</p>
                </div>

            </div>
        </div>
        <div>
            <button
                type="button"
                class="btn btn-primary"
                @click="launchBudgetCalc"
            >Demo</button>
            <button
                type="button"
                class="btn btn-primary"
                @click="openGitHubBC"
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

            }
        },
        methods: {
            launchBudgetCalc() {
                window.open("http://167.172.98.227/calculator");
            },
            openGitHubBC() {
                window.open("https://github.com/SamoJanezic/BudgetCalculator");
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