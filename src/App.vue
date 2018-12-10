<template>
  <div>
    <div v-if="participants.length > 0">
      <h1>Participants list</h1>
      <ol>
        <li v-for="person in participants"> {{ person.firstname }}
          {{person.lastname}}</li>

      </ol>
    </div>

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
            return {
                newPerson: {firstname: ' ', lastname: ' '},
                participants: []};
        },
        methods: {
            addNewParticipant() {
                if(!this.newPerson.lastname){
                    return;
                }
                this.participants.push(this.newPerson);
                this.newPerson = {};
            }
        }
    };
</script>