<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User name: {{name}}</p>
        <p>User age: {{age}}</p>
        <button @click="resetName">reset name</button>
        <button @click="resetFn">reset name</button>

    </div>
</template>

<script>
    import {eventBus} from '../main.js'

    export default {
        props: {
            name: {
                type: String,
                required: true,
                // default: 'max'
            },
            resetFn: Function,
            age: Number
        },
        methods:{
            resetName(){
                this.name = 'zenkai';
                this.$emit('nameWasReset', this.name)
            }
        },
        created() {
            eventBus.$on('ageWasEdited', (age)=>{
                this.age = age;
            })
        }
    }
</script>

<style scoped>
    div {
        background: lightcoral;
    }
</style>
