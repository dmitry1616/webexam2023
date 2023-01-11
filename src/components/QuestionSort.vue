<template>
    <select v-model="modelValue" @change="changeOption">
        <option disabled value="">Выберите из списка</option>
        <option v-for="option in options" :key="option.value" :value="option.value">{{ option.name }}</option>
    </select>
</template>
<script>
export default {
    name: 'my-select',
    props: {
        modelValue: {
            type: String
        },
        options: {
            tupe: Array,
            default: () => []
        }
    },
    methods: {
        changeOption(option){
            this.$emit("update:modelValue", option)
        }
    }
}

</script>
<style>

</style>