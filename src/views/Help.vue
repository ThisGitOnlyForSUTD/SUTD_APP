<template>
  <app-page back title="FAQ">
    <question-item
      v-for="q in questions"
      :key="q.title"
      :question="q"
    ></question-item>
  </app-page>
</template>


<script>
import AppPage from '../components/ui/AppPage'
import QuestionItem from '../components/question/QuestionItem'

export default {
  setup() {
    const questions = [
      {title: 'Что есть в данной системе?', text: 'Данное приложение реализовано для создания и обмена рабочими данными'},
      {title: 'Как тут реализована безопасность?', text: 'Все реализовано через Firebase, при помощи jwt token. Защита документов в свою очередь осуществляется благодаря ЦЭП и firebase'},
      {title: 'Список литературы', text: 'ля кто-нить вставте сюда ссылок'},
    ]

    return {questions}
  },
  components: {AppPage, QuestionItem}
}
</script>