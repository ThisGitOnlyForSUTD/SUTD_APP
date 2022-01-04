<template>
  <div class="sidebar" v-if="sidebar">
    <span class="sidebar-close" @click="close">&times;</span>

    <div class="sidebar-content">
      <p>Над данным проектом работали:
        <a class="creater-link" href="https://www.instagram.com/silence_rampage/">Сергей Жестов</a>
        <br>
        <a class="creater-link" href="https://www.instagram.com/under.dog.in/">Волошенко Данила</a>
        <br>
        <a class="creater-link" href="https://www.instagram.com/samoshkin.r/">Самошкин Роман</a>
      </p>
    </div>
  </div>
</template>

<script>
import {computed} from 'vue'
import {useStore} from 'vuex'

export default {
  setup() {
    const store = useStore()

    const sidebar = computed(() => store.state.sidebar)

    return {
      sidebar,
      close: () => store.commit('closeSidebar')
    }
  }
}
</script>

<style scoped>
.creater-link {
  color: rgba(18, 18, 18, 0.79);
}

.creater-link:hover{
  border-bottom: solid 1px;
}
</style>