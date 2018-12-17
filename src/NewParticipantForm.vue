<template>
    <div>
        <h3>New participant</h3>

            <form @submit.prevent="addNewParticipant()">
                <label>Firstname</label>
                <input type="text" v-model="newPerson.firstname">
                <label>Lastname</label>
                <input type="text" v-model="newPerson.lastname">
                <button>Add new participant</button>
            </form>

    </div>
</template>

<script>
    export default {
        data() {
            return {newPerson: {firstname: '', lastname: ''}};
        },
        methods: {
            addNewParticipant() {
                this.$emit('added', this.newPerson);
                this.newPerson = {};
            }

        }
    };
</script>