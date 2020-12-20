<template>
  <div class="inputs-list_input__input">
      {{ label }}
      <div class="input__radio-input" >
        <label v-for="item in values" :key="item" class="input__radio-input_label">
          {{ item }}
          <input
            class="input__radio-input_input"
            :type="inputType"
            :name="inputName"
            :value="item"
            @input="$emit('changeValue', $event.target.value, inputName)"
          />
        </label>
      </div>
      <slot />

  </div>
</template>

<script>
export default {
  name: "BoleansInput",
  props: {
    label: {
      type: String,
      required: true,
    },
    values: {
      type: Array,
      required: true,
    },
    inputType: {
      type: String,
      required: true,
    },
    inputName: {
      type: String,
      required: true,
    }
  },
  updated() {},
};
</script>

<style>
  .input__radio-input {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    height: 40px;
    margin-top: 0.5rem;
  }
  .input__radio-input_label {
    min-height: 1.5rem;
    padding-right: 1.5rem;
    margin-right: 0.5rem;

    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-end;
    align-items: center;
    box-sizing: border-box;

    font-size: 14px;
    cursor: pointer;
  }
  .input__radio-input_label:hover {
    color: #42b983;
  }

  .input__radio-input_input {
    width: 16px;
    height: 16px;
    margin: auto 8px auto 0;
    outline: none;

    /* border: 1px solid #D9D9D9;
      box-sizing: border-box;
      border-radius: 2px; */
    cursor: pointer;
  }
  .input__radio-input_input:focus {
    outline: solid 1px #42b983;
  }
</style>
