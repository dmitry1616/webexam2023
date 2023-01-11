<template>
    <form @submit.prevent>
        <h4>Задать вопрос</h4>
        <input v-model="question.title" class="input" type="text" placeholder="Вопрос">
        <input v-model="question.body" class="input" type="text" placeholder="Комментарий">
        <button 
        class="btn" 
        @click="createQuestion"
        >Отправить</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            question: {
                title: "",
                body: ""
            }
        }
    },

    methods: {
        createQuestion() {
            this.question.body
            this.question.title
            this.question.id = Date.now()
            this.question.userId = 0
            this.$emit("create", this.question)
            this.question = {
                title: "", body: ""
            }
            
        }
    }
}
</script>


<style>

</style>