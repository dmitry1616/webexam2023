<template>
    <div class="question" v-for="question in questions" v-bind:key="question">
        <div><strong>Пользователь </strong>{{ question.userId }}</div>
        <div><strong>Вопрос №</strong> {{ question.id }}</div>
        <div><strong>Вопрос:</strong> {{ question.title }}</div>
        <div><strong>Комментарий:</strong>{{ question.body }}</div>
    </div>


</template>

<script>
export default {
    props: {
        questions: {
            type: Array,
            required: true
        }
    }
}
</script>

<style>
.question {
    border: solid 1px black;
    padding: 15px;
}
.question div{
    padding: 5px;
}
</style>