<template>
    <div>
        <h2>This is pretend modal component</h2>
        <button @click="toggle">
            <template v-if="show">Hide</template>
            <template v-else>Show</template>
        </button>
        <div class="modal" v-if="show">
            <strong>Now you see this great modal!</strong>
            <p>Isn't it great</p>
            <button @click="toggle">x close</button>
        </div>

        <!-- Could also have a modal independent of the button/trigger and it could accept a show prop and emit a close event -->
        <!-- <modal-child @close="toggle" :show="show" /> -->
    </div>
</template>

<script>
export default {
    data: function () {
        return { show: false };
    },
    methods: {
        toggle: function () {
            this.show = !this.show;
        },
    },
};
</script>

<style scoped>
.modal {
    width: 300px;
    margin: 0px auto;
    padding: 20px 30px;
    background-color: pink;
    border-radius: 2px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
}
</style>
