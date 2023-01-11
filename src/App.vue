<template>
    <div>
        <question-list  :questions="questions"/>
    </div>
</template>

<script>
import QuestionList from "@/components/QuestionList.vue"
export default {
    components:
    {
        QuestionList
    },

    data() {
        return {
            questions: [
                { userId: 1, id: 2, title: "когда я закончу проект??", body: "ddddd" },
                { userId: 2, id: 3, title: "когдаssss я закончу проект??", body: "ddddd" },
                { userId: 3, id: 4, title: "ког4545роект??", body: "dddddddghd" },
                
            ]
        }
    }
}
</script>

<style>

</style>