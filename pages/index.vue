<template>
  <div id="app">
    <h1>Workout plan</h1>
    <LabelInput 
      nameOfExercise="Push-ups" 
      :numberOfSeries="3" 
      :weight="true" 
    />
  </div>
</template>
n
<script>
import LabelInput from '../components/labelInput.vue';

export default {
  name: 'TestPage',
  components: {
    LabelInput,
  },
};
</script>

<style>
#app {
  background-color: #FFF5E1;
}

h1 {
  font-size: 2em;
  color: #333;
  text-align: center;
  margin-top: 20px;
  font-family: 'Arial', sans-serif;
}
</style>

  