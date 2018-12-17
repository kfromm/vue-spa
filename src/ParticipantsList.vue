<template>
    <div v-if="list.length > 0">
        <h1>Participants list</h1>
            <ol>
                <li v-for="person in list">
                    {{ person.firstname }}
                    {{ person.lastname }}
                </li>
            </ol>
    </div>
</template>

<script>
    export default {
        props: ['list']
    };
</script>

<style>
    ol{
        color:green;
    }
</style>