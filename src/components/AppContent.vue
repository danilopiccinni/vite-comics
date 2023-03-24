<script>

    export default {
        data() {
            return {
                content : '--> Content goes here <--'
            }
        }
    }

</script>

<template>

    <div>
        <h1>
            {{ content }}
        </h1>
    </div>

</template>

<style scoped lang="scss">

    div {
        display: flex;
        align-items: center;

        align-items: center;
        padding: 25px 100px;


        height: 150px;
        background-color: #1c1c1c;
        
        h1 {
            color: white;
        };
    }

</style>