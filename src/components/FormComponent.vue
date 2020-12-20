<template>
  <div class="form">
    <div class="form__section">
      <div class="section_title">
        Личные данные:
      </div>
      <div class="section__inputs-list">
        <TextInput
          label="Фамилия*"
          :value="this.inputsList.lastName"
          placeholder="Karpov"
          inputName="lastName"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Имя*"
          :value="this.inputsList.name"
          placeholder="Karpov"
          inputName="name"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Отчество"
          :value="this.inputsList.patronymic"
          placeholder="Viacheslavovich"
          inputName="patronymic"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Дата рождения*"
          :value="this.inputsList.birthDate"
          placeholder="дд.мм.гггг"
          inputName="birthDate"
          inputType="date"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Номер телефона*"
          :value="this.inputsList.phoneNumber"
          placeholder="79602589363"
          inputName="phoneNumber"
          inputType="tel"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <BoleansInput
          label="Пол"
          inputName="gender"
          :values="['мужчина', 'Женщина']"
          inputType="radio"
          @changeValue="onRadioChangeHandler"
        />
        <BoleansInput
          label="Группа клиентов*"
          inputName="clientGroup"
          :values="['VIP', 'Проблемные', 'ОМС']"
          inputType="checkbox"
          @changeValue="onCheckboxChangeHandler"
        />
        <BoleansInput
          label="Лечащий врач"
          inputName="doctor"
          :values="['Иванов', 'Захаров', 'Чернышева']"
          inputType="radio"
          @changeValue="onRadioChangeHandler"
        />
        <BoleansInput
          label="Не отправлять СМС"
          inputName="shouldSendSms"
          :values="['Я не хочу получать смс']"
          inputType="checkbox"
          @changeValue="onCheckboxChangeHandler"
        />
      </div>
    </div>

    <div class="form__section">
      <div class="section_title">
        Адрес:
      </div>
      <div class="section__inputs-list">
        <TextInput
          label="Индекс*"
          :value="this.inputsList.index"
          placeholder="198504"
          inputName="index"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Страна"
          :value="this.inputsList.country"
          placeholder="Россия"
          inputName="country"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Область"
          :value="this.inputsList.region"
          placeholder="Санкт-Петербургская агломерация"
          inputName="region"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Город*"
          :value="this.inputsList.city"
          placeholder="Санкт-Петербург"
          inputName="city"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Улица"
          :value="this.inputsList.street"
          placeholder="Ботаническая"
          inputName="street"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Дом"
          :value="this.inputsList.house"
          placeholder="18"
          inputName="house"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
      </div>
    </div>

    <div class="form__section">
      <div class="section_title">
        Адрес:
      </div>
      <div class="section__inputs-list">
        <BoleansInput
          label="Тип документа"
          inputName="identificationType"
          :values="['Паспорт', 'Свидетельство о рождении', 'Вод. удостоверение']"
          inputType="radio"
          @changeValue="onRadioChangeHandler"
        />
        <TextInput
          label="Серия"
          :value="this.inputsList.identificationSeries"
          placeholder=""
          inputName="identificationSeries"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Номер"
          :value="this.inputsList.identificationNumber"
          placeholder=""
          inputName="identificationNumber"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Кем выдан"
          :value="this.inputsList.identificationIssuedBy"
          placeholder=""
          inputName="identificationIssuedBy"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>
        <TextInput
          label="Дата выдачи*"
          :value="this.inputsList.identificationIssuedDate"
          placeholder="дд.мм.гггг"
          inputName="identificationIssuedDate"
          inputType="text"
          @changeValue="onTextChangeHandler"
        >
          <!-- <div class="error" v-if="!$v.inputsList[key].value.required">Field is required </div>
          <div class="error" v-if="!$v.inputsList[key].value.minLength">{{key}} must have at least {{$v.inputsList[key].value.$params.minLength.min}} letters.</div> -->
        </TextInput>

      </div>
    </div>
    <!-- <div class="error" v-if="!$v.name.minLength">Name must have at least {{$v.name.$params.minLength.min}} letters.</div>

    <div class="form-group" :class="{ 'form-group--error': $v.age.$error }">
      <label class="form__label">Age</label>
      <input class="form__input" v-model.trim.lazy="$v.age.$model"/>
    </div>
    
      :validate="item.validate"
    <div class="error" v-if="!$v.age.between">
      Must be between {{$v.age.$params.between.min}} and {{$v.age.$params.between.max}}
    </div>
    
    <h1>Адрес:</h1>
    
    <h1>Паспорт:</h1>
    <span tabindex="0">
      Blur to see changes
    </span> -->

    <div class="form__submit">
      <button @click="onSubmitHandler" >
        Взгляни что ты наделал
      </button>
    </div>

    <template v-if="submitted" >
      <SubmittedModal
        :state="this.inputsList"
        :clickHandler="this.onSubmitHandler" />
      <div class="submitted-modal__overlay" @click="this.onSubmitHandler"/>
    </template>
  </div>
</template>

<script>
import { required, minLength } from 'vuelidate/lib/validators'
import TextInput from './common/TextInput.vue'
import BoleansInput from './common/BoleansInput.vue'
import SubmittedModal from './common/submittedModal'

export default {
  name: 'FormComponent',
  components: {
    TextInput, BoleansInput, SubmittedModal
  },
  data() {
    return {
      inputsList: {
        lastName: "",
        name: "",
        patronymic: "",
        birthDate: "",
        phoneNumber: "7",
        gender: "",
        clientGroup: [],
        doctor: "",
        shouldSendSms: [],
        index: "",
        country: "",
        region: "",
        city: "",
        street: "",
        house: "",
        identificationType: "",
        identificationSeries: "",
        identificationNumber: "",
        identificationIssuedBy: "",
        identificationIssuedDate: ""
      },
      submitted: false
    }
  },
  methods: {
    onTextChangeHandler(value, inputName) {
      this.inputsList[inputName] = value
      // this.$v.inputsList[inputName].$touch()
    },
    onRadioChangeHandler(value, inputName) {
      this.inputsList[inputName] = value
    },
    onCheckboxChangeHandler(value, inputName) {
      this.inputsList[inputName].includes(value)?
        this.inputsList[inputName] = this.inputsList[inputName].value.filter( item => item !== value ):
        this.inputsList[inputName].push(value)
      // this.$v.inputsList[inputName].$touch()
      // console.log(this.$v.inputsList[inputName])
    },
    onSubmitHandler() {
      this.submitted = !this.submitted
    }
  },
  validations: {
    inputsList: {
      name: {
        value: {
          required,
          minLength: minLength(4)
        }
      },
      lastName: {
        value: {
          required,
          minLength: minLength(4)
        }
      },
      patronymic: {
        value: {
          required: false,
          minLength: minLength(4)
        }
      },
      birthDate: {
        value: {
          required,
          minLength: minLength(4)
        }
      },
      phoneNumber: {
        value: {
          required,
          minLength: minLength(11)
        }
      }
    }
  }
}
</script>

<style >
  .form {
    max-width: 1280px;
    margin: 0 auto;
    padding: 3rem;

    display: flex;
    flex-direction: column;
  }
  .form__section {
    margin-bottom: 3rem;
  }
  .section_title {
    font-size: 2rem;
    text-align: start;
    margin-bottom: 2rem;
  }
  .section__inputs-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
    
    border: 1px solid rgba(66, 185, 131, 0.2);
    border-radius: 1rem;
  }
  .inputs-list_input__input {
    position: relative;
    width: 50%;
    padding: 1.5rem 2rem;
    box-sizing: border-box;

    text-align: left;
    font-size: 1rem;
    cursor: pointer;
  }
  .form__submit {
    width: 100%;
    display: flex;
    justify-content: center;
  }
  button {
    max-width: 343px;
  }
  .submitted-modal__overlay {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 5;
  }
  ::-webkit-calendar-picker-indicator {
    background-color: rgba(66, 185, 131, 0.4);
    border-radius: 3px;
    cursor: pointer;
  }
  ::-webkit-calendar-picker-indicator:hover {
    background-color: rgba(66, 185, 131, 0.8);
  }
  ::-webkit-datetime-edit {
    cursor: text;
  }

  @media (max-width: 768px) {
    .inputs-list_input__input {
      width: 100%;
    }
  }
</style>