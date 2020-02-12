<template>
  <div>
    <div class="row">
      <div class="col-3 left no-padding">
        <app-left
          @componentChange="currentComponent = $event"
        ></app-left>
      </div>
      <div class="col-9 right no-padding">
        <app-right
          :component="currentComponent"
        ></app-right>
      </div>
    </div>
  </div>
</template>

<script>
  import MainPage from './components/MainPage.vue';
  import LeftSide from './components/LeftSide.vue';
  import RightSide from './components/RightSide.vue';

  export default {
    components: {
      appMain: MainPage,
      appLeft: LeftSide,
      appRight: RightSide,
    },

    data () {
      return {
        currentComponent: 'appProject',
      }
    }
  }
</script>

<style lang="scss">
  body {
    background-color:transparent;
  }
  html {
    background-image: linear-gradient(
      rgba(0, 0, 0, 0.25),
      rgba(0, 0, 0, 0.75)
      ),
      url('../src/assets/bohinj.jpg')
      ;
    background-size: cover;
    background-position: center;
    height: 100%;
    width: 100%;
  }
.left {
  border-right: 1px solid black;

}
.right {
  border-left: 1px solid black;
  background-color: rgba(0, 0, 0, 0.25);
  height: 100vh;
}
.row {
  width: 100%;
  margin: 0;
}
.no-padding {
  padding-left: 0px;
  padding-right: 0px;
}
</style>
