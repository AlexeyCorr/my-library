<template>
  <div id="app" class="library container">
    <h1 class="library__title">Библиотека компонентов</h1>
    <section class="library__block" v-for="block in libraryBlocks" :key="block.id">
      <h2 class="library__subtitle">{{ block.title }}</h2>
      <component class="library__component" :is="block.component"></component>
    </section>
  </div>
</template>

<script>
import Basic from './components/Basic.vue'
import BurgerToggle from './components/BurgerToggle.vue'
import Rating from './components/Rating.vue'
import Toggles from './components/Toggles.vue'
import Tabs from './components/Tabs.vue'
import MainTitle from './components/MainTitle.vue'
import Popup from './components/Popup.vue'

export default {
  name: 'app',
  components: {
    Basic,
    BurgerToggle,
    Rating,
    Toggles,
    Tabs,
    MainTitle,
    Popup,
  },
  data() {
    return {
      libraryBlocks: [
        {
          id: 1,
          title: 'Текст и теги',
          component: 'Basic'
        },
        {
          id: 2,
          title: 'Бургер',
          component: 'BurgerToggle'
        },
        {
          id: 3,
          title: 'Рейтинг на CSS',
          component: 'Rating'
        },
        {
          id: 4,
          title: 'Чекбоксы, радио кнопки..',
          component: 'Toggles'
        },
        {
          id: 5,
          title: 'Табы',
          component: 'Tabs'
        },
        {
          id: 6,
          title: 'Заголовок',
          component: 'MainTitle'
        },
        {
          id: 6,
          title: 'Модальное окно',
          component: 'Popup'
        },
      ],
    }
  }
}
</script>

<style lang="scss">
@import "~normalize.css/normalize.css";

*,
*::before,
*::after {
  box-sizing: border-box;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;

  padding: 15px;
}

.container {
  min-width: 290px;
  margin: 0 auto;

  @media (min-width: 768px) {
    width: 728px;
  }

  @media (min-width: 1000px) {
    width: 950px;
  }

  @media (min-width: 1200px) {
    width: 1150px;
  }
}

.library__title {
  font-size: 32px;
  color: #000;
  text-align: center;

  margin: 0 0 15px;
}

.library__block {
  padding: 10px 20px;
  border: 3px dashed #eee;
  margin: 0 0 30px;
}

.library__subtitle {
  font-size: 26px;
  color: #000;

  position: relative;
  padding-left: 25px;
  margin: 0 0 15px;

  &::before {
    content: "";
    position: absolute;
    left: 0;
    top: 14px;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
    background: url("assets/img/icon-elem.svg") no-repeat center / cover;
  }
}

.library__component {
  padding-left: 25px;
}
</style>
