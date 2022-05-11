<template>
  <div id="step-one">
    <div id="navigation"></div>
    <div id="form-wrapper">
      <div class="input-group">
        <label for="name">
          <div v-if="showLabelName" class="input-label">Name</div>
          <input
            @focus="showLabelName = !showLabelName"
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
    .input-group {
      width: 400px;
      height: 60px;
      .input-field {
        outline: none;
        border: none;
      }
    }
  }
}
</style>
>
