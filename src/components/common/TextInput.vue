<template>
  <div class="inputs-list_input__input">

    <label class="input__text-input_label">
      {{ label }}
      <input
        class="input__text-input_input"
        :type="inputType"
        :value="value"
        :placeholder="placeholder"
        @input="$emit('changeValue', $event.target.value, inputName)"
      />
    </label>
    
    <slot/>
    <!-- v-model.trim="$v.name.$model" -->
  </div>
</template>

<script>

export default {
  name: 'TextInput',
  props: {
    label: {
      type: String,
      required: true
    },
    value: {
      type: String,
      required: true
    },
    placeholder: {
      type: String,
      required: false
    },
    inputType: {
      type: String,
      required: true
    },
    inputName: {
      type: String,
      required: true
    }
    // validate: {
    //   type: Object,
    //   default: () => {}
    // }
  },
  // updated() {
  //   console.log(this.value);
  // }
}
</script>

<style scoped>
  .input__text-input_label {
    display: flex;
    flex-direction: column;
    align-items: flex-start;

    max-width: 400px;
    font-weight: bold;
  }
  .input__text-input_input {
    height: 40px;
    width: 100%;
    margin-top: 0.5rem;
    padding: 8px 12px;

    background-color: rgba(1, 4, 9, 0.3);
    color: #C9D1D9;
    border: 1px solid #21262D;
    box-sizing: border-box;
    border-radius: 5px;
    outline: none;

    font-style: normal;
    text-align: left;
  }

  .input__text-input_input:hover {
    border: 1px solid #42b983;
  }

  .input__text-input_input:focus {
    border: 1px solid #42b983;
    box-shadow: 0px 0px 4px rgba(66, 185, 131, 0.5);
  }

  .input__text-input_input::placeholder {
    color: #484f58;
  }
  /* .form__input_text-input:disabled {
    background: #F5F5F5;
    border: 1px solid #D9D9D9;
  } */

</style>
