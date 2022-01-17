<template>
    <div style="width: 400px; border: solid 2px;">
        <h2>This is another Component</h2>
        <button v-on:click="toggle">
            <template v-if="show">Hide</template>
            <template v-else>Show</template>
        </button>
        <div>
            <strong v-if="show">Now you see me!</strong>
        </div>
    </div>

</template>

<script>
    export default {
        data: function() {
            return { show: false }
        },
        methods: {
            toggle: function() {
                this.show = !this.show
            }
        }
    }
</script>
