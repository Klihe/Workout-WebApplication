<template>
  <div class="all">
    <div class="label">
      <label class="label-text">{{ nameOfExercise }}</label>
      <label class="label-text">series: {{ numberOfSeries }}</label>
    </div>
    <div v-for="index in numberOfSeries" :key="'input' + index" class="input">
      <input v-if="weight" type="number" v-model="weightSeriesNumbers[index]" placeholder="weight [kg]" class="input-field" />
      <input type="number" v-model="repSeriesNumbers[index]" placeholder="reps" class="input-field" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'LabelInput',
  props: {
    nameOfExercise: String,
    numberOfSeries: Number,
    weight: Boolean,
  },
  data() {
    return {
      repSeriesNumbers: [this.numberOfSeries],
      weightSeriesNumbers: [this.numberOfSeries],
    };
  },
};
</script>

<style>
.all {
  display: flex;
  justify-content: center;
}

.label {
  display: flex;
  flex-direction: column;
  font-family: 'Arial', sans-serif;
  font-size: 1.2em;
  margin-top: 10px;
}

.label-text {
  margin-bottom: 5px;
}

.input {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-top: 10px;
}

.input-field {
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-left: 2px;
  margin-right: 2px;
  margin-bottom: 2px;
}
</style>