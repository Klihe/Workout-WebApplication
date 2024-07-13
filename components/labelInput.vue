<template>
    <div>
      <label for="inputField">{{ label }}</label>
      <input type="text" id="inputField" v-model="inputValue" />
    </div>
  </template>
  
  <script>
  export default {
    name: 'LabelInput',
    props: {
      label: {
        type: String,
        required: true
      }
    },
    data() {
      return {
        inputValue: ''
      };
    }
  };
  </script>
  
  <style>
  </style>