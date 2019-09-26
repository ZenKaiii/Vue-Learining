<template>
    <div>
        <app-status v-for="server in 5"></app-status>
    </div>
</template>

<script>
    import ServerStatus from "./ServerStatus";
    export default {
        components:{
            "app-status":ServerStatus
        }
    }
</script>

<style scoped>

</style>