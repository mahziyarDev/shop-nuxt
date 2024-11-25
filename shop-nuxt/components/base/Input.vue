<template>
  <div class="form-element-row">
    <label class="label fs-7">
      {{label}}
    </label>
    <input
        :name="name"
        :value="modelValue"
        :type="type"
        :class="['form-control',{'error-input':errorMessage}]"
        :placeholder="placeholder"
        @autocomplete="autocomplete"
        @input="handelInputChange"
    />
    <span class="text-danger" v-if="errorMessage && !ignoreErrorMessage">{{errorMessage}}</span>
  </div>
</template>

<script setup lang="ts">
import {useField} from 'vee-validate'
const props = defineProps({
  name:{
    type:String,
    required:true,
  },
  modelValue:{
    default:"",

  },
  label:{
    type:String,
    default:"",
  },
  placeholder:{
    type:String,
    default:""
  },
  autocomplete:{
    type:Boolean,
    default:false
  },
  type:{
    type:String,
    default:"text",
  },
  ignoreErrorMessage:{
    type:Boolean,
    default:false,
  }

})
const {
  errorMessage,
  value:inputValue,
  handleChange,
  setValue,
} =useField(
    props.name,
    undefined,{initialValue:props.modelValue}
);

const emit = defineEmits(["update:modelValue"]);
watch(
    ()=>props.modelValue,
    (val)=>setValue(val)
);
const handelInputChange = (e:any)=>{
  emit("update:modelValue", e.target.value);
  handleChange(e);
}

</script>

<style scoped>

</style>