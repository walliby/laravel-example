<template>
    <div class="modal" v-if="show">
        <strong>This is now a separate component!</strong>
        <p>Isn't it great</p>
        <button @click="$emit('close')">x close</button>
    </div>
</template>

<script>
export default {
    props: ["show"],
};
</script>

<style scoped>
.modal {
    width: 300px;
    margin: 0px auto;
    padding: 20px 30px;
    background-color: lightblue;
    border-radius: 2px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
}
</style>
