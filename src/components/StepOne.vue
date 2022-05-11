<template>
  <div id="step-one">
    <div id="navigation"></div>
    <div class="headers">
      <h1>Delivery Details</h1>
    </div>
    <div id="form-wrapper">
      <div class="input-group">
        <label for="name">
          <div
            :style="[
              showLabelName ? { display: 'block' } : { display: 'none'},
            ]"
            class="input-label"
          >
            Name
          </div>
          <input
            @focus="showLabelName = true"
            @blur="showLabelName = false"
            class="input-field"
            id="name"
            placeholder="name"
            type="text"
          />
        </label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StepOne',
  data() {
    return {
      showLabelName: false,
    };
  },
};
</script>

<style lang="scss" scoped>
#step-one {
  #form-wrapper {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    .input-group {
      padding: 12px 15px;
      height: 40px;
      font-family: "Inter";
      background: #ffffff;
      border: 1px solid #1bd97b;
      .input-label {
        font-weight: 500;
        font-size: 13px;
        height: 16px;
        color: #1bd97b;
        mix-blend-mode: normal;
        opacity: 0.8;
      }
      .input-field {
        outline: none;
        border: none;
        font-weight: 700;
        font-size: 16px;
        line-height: 19px;
        color: #2d2a40;
      }
      .input-field::placeholder {
        font-weight: 500;
        color: #000000;
        mix-blend-mode: normal;
        opacity: 0.4;
      }
      .input-field:-ms-input-placeholder {
        /* Internet Explorer 10-11 */
        color: #000000;
      }
      .input-field::-ms-input-placeholder {
        /* Microsoft Edge */
        color: #000000;
      }
    }
  }
}
</style>
>
