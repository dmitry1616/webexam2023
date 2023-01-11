<template>
    <div>
        <div><button @click="">Сортировать</button><select name="asd" id=""></select></div>

        <button @click="fetchQuestions">Получить вопросы</button>
        <button @click="showDialog">Задать вопрос</button>
        <QuestionModal v-model:show="dialogVisible"><QuestionNew @create="createQuestion" /></QuestionModal>
        
        <question-list :questions="questions" />
    </div>
</template>

<script>
import QuestionList from "@/components/QuestionList.vue"
import QuestionNew from "@/components/QuestionNew.vue"
import QuestionModal from "@/components/QuestionModal.vue"
import QuestionSort from "./components/QuestionSort.vue"
import axios from "axios"
export default {
    components:
    {
        QuestionList, QuestionNew, QuestionModal, QuestionSort
    },

    data() {
        return {
            questions: [],
            dialogVisible: false,
        }
    },
    methods: {
        createQuestion(question) {
            this.questions.push(question);
            this.dialogVisible = false;
        },
        showDialog(){
            this.dialogVisible = true;
        },
        async fetchQuestions(){
            try {
                const response = await axios.get("https://jsonplaceholder.typicode.com/posts?_limit=10");
                this.questions = response.data;
            } catch (error) {
                alert("Произошла ошибка")
            }
        }
    }
}
</script>


<style>

</style>