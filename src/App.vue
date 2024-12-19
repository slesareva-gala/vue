<template>
  <div id="app">
    <h1>Тема урока: {{ title }}</h1>

    <ul>
      <list-item :text="posts[0].text" :icon="posts[0].icon" />
      <list-item :text="posts[1].text" :icon="posts[1].icon" />
      <list-item :text="posts[2].text" :icon="posts[2].icon" />
    </ul>
    <span class="total">Всего строк: {{ totalCount }}</span>

  </div>
</template>

<script>
import ListItem from '@/components/ListItem.vue';

export default {
  components: { ListItem },
  comments: { ListItem },

  data() {
    return {
      title: 'Props',
      posts: [
        {
          id: 0,
          text: 'текст первый',
          icon: 'setting.png',
          checked: true,
        },
        {
          id: 1,
          text: 'текст второй',
          icon: 'user.png',
          checked: false,
        },
        {
          id: 2,
          text: 'текст тректий',
          icon: 'phone.png',
          checked: false,
        }
      ]
    }
  },
  computed: {
    totalCount() {
      return this.posts.length + ' шт'
    }
  }
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;

  li {
    display: flex;
    align-items: center;
    margin-bottom: 10px;

    img {
      margin-right: 10px;
    }


    &:hover {
      color: red;
    }

    &.checked {
      color: blue;
    }
  }

  li.list-item {
    font-size: 1.3rem;
  }
}
</style>
