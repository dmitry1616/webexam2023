<template>
    <form @submit.prevent>
        <h4>Задать вопрос</h4>
        <input v-model.trim="question.title" class="input" type="text" placeholder="Вопрос">
        <input v-model.trim="question.body" class="input" type="text" placeholder="Комментарий">
        <button 
        class="btn" 
        @click="createQuestion"
        >Отправить</button>
        <p>{{ this.question.valid }}</p>
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
            this.question.valid = "Введите корректные значения"
            this.question.body
            this.question.title
            if (this.question.title == "" || this.question.body == "")
            {
                this.question.valid;
            }
            else{
            this.question.id = Date.now()
            this.question.userId = 0
            this.$emit("create", this.question)
            this.question = {
                title: "", body: ""
            }
        }
            
        }
    }
}
</script>


<style>

</style>