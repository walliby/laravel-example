<template>
    <div class="container" style="width: 400px; border: solid 2px;">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>
                    <button v-on:click="addItem">Click me to add item</button>
                    <ol>
                        <li v-for="(item, index ) in items" :key="index">
                            {{ item }}
                        </li>
                    </ol>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data: function() {
            return { items: ["first"] }
        },
        methods: {
            addItem: function() {
                this.items.push("another")
            }
        }
    }
</script>
