<template>
  <div class="submitted-modal">
    <div>
      <h1>Пользователь создан</h1>
      <div class="modal-user-info">
        <div v-for="(item, key) in state" :key="key">
          {{item}}
        </div>
      </div>
    </div>
    <button
      class="modal__button"
      @click="clickHandler"
    >
      Ура!
    </button>
  </div>
</template>

<script>

  export default ({
    name: "submittedModal",
    props: {
      state: {
        type: Object,
        required: true
      },
      // name: {
      //   type: String,
      //   required: true
      // },
      // patronymic: {
      //   type: String,
      //   required: true
      // },
      // birthDate: {
      //   type: String,
      //   required: true
      // },
      clickHandler: {
        type: Function,
        required: true
      }
    }
  })
</script>

<style scoped>
  .submitted-modal {
    position: fixed;
    width: 50%;
    height: 50%;
    top: 50%;
    left: 50%;
    padding: 2rem;
    display: flex;
    justify-content: center;

    background-color: #0D1117;
    transform: translate3d(-50%, -50%, 0);
    border: 1px solid rgba(66, 185, 131, 0.2);
    border-radius: 2rem;
    z-index: 10;
  }
  .modal-user-info {
    display: flex;
    flex-wrap: wrap;
  }
  .modal-user-info div {
    width: 30%;
    margin: 0.5rem;
  }
  button {
    position: absolute;
    bottom: 3rem;
    width: 100%;
    max-width: 360px;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;

    background: #42b983;
    box-sizing: border-box;
    border: none;
    border-radius: 5px;
    outline: none;

    color: #FFFFFF;
    font-family: "SF Pro Display Regular";
    text-align: center;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;

    cursor: pointer;
  }

  button:hover {
    background: #40A9FF;
  }

  button:active {
    background: #096DD9;
  }

  .Disabled {
    background: #E8E8E8;
    border: 1px solid #D9D9D9;
    color: #BCBCBC;
    cursor: default;
  }

  .Disabled:hover {
    background: #E8E8E8;
  }
</style>