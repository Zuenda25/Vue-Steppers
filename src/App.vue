<template>
  <div id="app">
    <div id="step-bar">
      <div class="step-item">
        <button class="step-item-count" @click="showStepOne()">1</button>
        <div class="step-item-title">Delivery</div>
      </div>
      <ChevronRight :size="24" fillColor="#FF8A00" />
      <div class="step-item">
        <button
          class="step-item-count"
          @click="showStepTwo()"
          :class="{ 'not-active-item': !stepTwo }"
        >
          2
        </button>
        <div class="step-item-title">Payment</div>
      </div>
      <ChevronRight :size="24" fillColor="#FF8A00" />
      <div class="step-item">
        <button class="step-item-count" :class="{ 'not-active-item': !stepThree }">3</button>
        <div class="step-item-title">Finish</div>
      </div>
    </div>
    <div id="main-content">
      <div id="section-form">1</div>
      <div id="section-submit">
        <div id="submit-content">
          <div id="submit-content-wrapper">
            <h1>Summary</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChevronRight from 'vue-material-design-icons/ChevronRight.vue';

export default {
  name: 'App',
  components: {
    ChevronRight,
  },
  data() {
    return {
      stepOne: true,
      stepTwo: false,
      stepThree: false,
    };
  },
};
</script>

<style lang="scss">
h1 {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 44px;
  color: #ff8a00;
}

body {
  background: #fffae6;
  margin: 0;
  padding: 0;
  #app {
    font-family: "Inter", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    box-sizing: border-box;
    #step-bar {
      position: absolute;
      display: inline-flex;
      justify-content: space-around;
      align-items: center;
      width: 50vw;
      height: 70px;
      left: 25vw;
      top: 20px;
      background: #fffae6;
      border-radius: 35px;
      .step-item {
        display: inline-flex;
        font-family: "Inter";
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 19px;
        .step-item-count {
          border: none;
          text-align: center;
          width: 30px;
          height: 30px;
          background: #ff8a00;
          color: #ffffff;
          mix-blend-mode: normal;
          border-radius: 15px;
        }
        .not-active-item {
          color: #ff8a00;
          background: rgba(255, 138, 0, 0.2);
          mix-blend-mode: normal;
        }
        .step-item-title {
          margin-left: 10px;
          padding-top: 6px;
          color: #ff8a00;
        }
      }
    }
    #main-content {
      display: grid;
      grid-template-columns: 2.75fr 1.25fr;
      width: calc(100vw - 100px);
      min-height: calc(100vh - 120px);
      margin: 55px 50px;
      background: #ffffff;
      box-shadow: 2px 10px 20px rgba(255, 138, 0, 0.1);
      border-radius: 4px;
      #section-submit {
        padding: 50px 20px 20px 0px;
        #submit-content {
          min-height: calc(100vh - 190px);
          border-left: 1px solid #ff8a00;
          #submit-content-wrapper {
            margin-left: 20px;
          }
        }
      }
    }
  }
}
</style>
