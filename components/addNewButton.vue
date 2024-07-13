<template>
    <div class="all">
        <div class="inputs">
            <input type="text" v-model="name" placeholder="Name of exercise" class="input-field" />
            <input type="number" v-model="series" placeholder="Number of series" class="input-field" />
            <input type="checkbox" v-model="weight" class="input-field" />
        </div>
        <div class="button">
            <label>Weight</label>
            <button @click="addNewExercise" class="add-button">Add new exercise</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AddNewButton',
    data() {
        return {
            exercises: [],
            name: '',
            series: '',
            weight: false
        };
    },
    methods: {
        addNewExercise() {
            if (this.name === '' || this.series === '' || this.series < 1) {
                return;
            }
            
            this.exercises.push({
                name: this.name,
                series: this.series,
                weight: this.weight
            });
            this.$emit('add:exercises', this.exercises);

            // Clear the inputs
            this.name = '';
            this.series = '';
            this.weight = false;
        }
    }
};
</script>

<style>
.all{
    display: flex;
    justify-content: center;
}
</style>