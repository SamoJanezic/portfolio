<template>
    <div>
        <div v-if="comp">
            <preview-project :is="selected" @wentBack="comp=!comp"></preview-project>
        </div>
        <div v-else>
            <h1 class="project title">My projects</h1>
            <p class="text">These are few projects i've worked on in the last year</p>
            <div class="row">
                <div class="col-6">
                    <img
                    src="../../assets/Screenshot-tetris.png"
                    class="preview"
                    title="Tetris-v3"
                    @click="showTetris"
                    >
                </div>
                <div class="col-6">
                    <img
                    src="../../assets/Screenshot-budget_calc.png"
                    class="preview"
                    title="Budget Calculator"
                    @click="showBudget"
                    >
                </div>
            </div>
        </div>
    </div>
</template>


<script>
    import tetris from "./Projects/Tetris";
    import budgetCalc from "./Projects/Budget calc"

    export default {
        components:{
            proTetris: tetris,
            proBudgetCalc: budgetCalc,
        },
        data: () => {
            return {
                comp: false,
                selected: '',

            }
        },
        methods: {
            showTetris() {
                this.comp = !this.comp;
                this.selected = 'proTetris';
                console.log(this.selected);
            },
            showBudget() {
                this.comp = !this.comp;
                this.selected = 'proBudgetCalc';
                console.log(this.selected);
            }
        }
    }
</script>


<style scoped>
    .title {
        padding: 6% 0 0% 0;
        color:rgba(255, 255, 255, 0.678);
    }
    .text {
        color: rgba(255, 255, 255, 0.40);
        padding: 0% 10%;
    }
    .preview {
        width: 90%;
        cursor: pointer;
    }
</style>