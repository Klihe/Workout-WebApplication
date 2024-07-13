<template>
    <div id="app">
      <LabelInput v-for="index in inputs.length" :key="index" :label="'Enter your text: '+ (index)" />
      <button @click="buttonClicked">add new</button>
    </div>
  </template>
  
  <script>
  import LabelInput from '../components/labelInput.vue';
  
  export default {
    name: 'App',
    components: {
      LabelInput
    },
    data() {
      return {
        inputs: []
      };
    },
    methods: {
      buttonClicked() {
        this.inputs.push({});
      }
    }
  };
  </script>
  
  <style>
  </style>
  