<template>
  <div id="app">
    <h1>Workout plan</h1>
    <addNewButton @add:exercises="addExercise"/>
    <LabelInput
      v-for="(exercise, index) in exercisesList"
      :key="index"
      :nameOfExercise="exercise.name"
      :numberOfSeries="exercise.series"
      :weight="exercise.weight"
    />
  </div>
</template>
n
<script>
import LabelInput from '../components/labelInput.vue';
import AddNewButton from '../components/addNewButton.vue';

export default {
  name: 'TestPage',
  components: {
    LabelInput,
    AddNewButton,
  },
  data() {
    return {
      exercisesList: [],
    };
  },
  methods: {
    addExercise(exercise) {
      this.exercisesList = exercise;
    },
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

  