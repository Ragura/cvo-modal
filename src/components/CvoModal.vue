<template>
    <div class="modal" v-show="open" @click="$emit('close')">
        <div class="modal-box" @click.stop>
            <h1>{{ titel }}</h1>
            <hr>
            <p>{{ boodschap }}</p>
            <button @click="$emit('close')">Sluiten</button>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            open: Boolean,
            titel: String,
            boodschap: String
        },
    }
</script>

<style scoped>
    .modal {
        display: flex;
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        overflow: auto;
        z-index: 1;
        background-color: rgba(0,0,0,0.4);
        justify-content: center;
        align-items: center;
    }

    .modal-box {
        width: 400px;
        padding: 2em;
        z-index: 2;
        background-color: lemonchiffon;
        text-align: center;
    }

    
</style>