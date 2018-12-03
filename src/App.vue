<template>
  <div>
    <h1>Clicked {{ times }} times</h1>
    <button @click="iAmClicked()">Click me!</button>
    <button @click="Reset()">reset</button>
  </div>
</template>

<script>
    export default {
        data() {
            return {times: 0}
        },
        methods: {
            iAmClicked() {
                this.times = this.times + 1;
            },
            Reset(){
                this.times = 0;
            }
        }
    };
</script>