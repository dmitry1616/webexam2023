<template>
    <div>
        <QuestionNew @create="createQuestion" />
        <question-list :questions="questions" />


    </div>
</template>

<script>
import QuestionList from "@/components/QuestionList.vue"
import QuestionNew from "@/components/QuestionNew.vue"
export default {
    components:
    {
        QuestionList, QuestionNew
    },

    data() {
        return {
            questions: [
                { userId: 1, id: 2, title: "когда я закончу проект??", body: "ddddd" },
                { userId: 2, id: 3, title: "когдаssss я закончу проект??", body: "ddddd" },
                { userId: 3, id: 4, title: "ког45dd45роект??", body: "dddddddghd" },

            ],
        }
    },
    methods: {
        createQuestion(question) {
            this.questions.push(question);
        }
    }
}
</script>

<style>

</style>