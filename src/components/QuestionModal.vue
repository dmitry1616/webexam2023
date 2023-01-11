<template>
    <div class="dialog" v-if="show" @click.stop="hideDialog">
        <div @click.stop class="dialog__content">
            <slot></slot>
        </div>
    </div>
</template>


<script>
export default {
    name: "my-dia",
    props: {
        show: {
            type: Boolean,
            default: false
        }

    },
    methods: {
        hideDialog() {
            this.$emit('update:show', false)

        }
    }
}
</script>

<style scoped>
.dialog {
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.39);
    position: fixed;
    display: flex;
    transition: 1s;

}

.dialog__content {
    margin: auto;
    background: white;
    border-radius: 15px;
    min-height: 100px;
    min-width: 200px;
    padding: 20px;
}
</style>
