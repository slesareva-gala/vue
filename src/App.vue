<template>
  <div id="app">
    <h1>Тема урока: {{ title }}</h1>

    <ul>
      <li class="list-item" :class="posts[0].checked ? 'checked' : ''">
        <img :src="require(`@/assets/images/${posts[0].icon}`)" :alt="posts[0].icon">
        <span>{{ posts[0].text }}</span>
      </li>
      <li :class="posts[1].checked ? 'checked' : ''">
        <img :src="require(`@/assets/images/${posts[1].icon}`)" :alt="posts[1].icon">
        <span>{{ posts[1].text }}</span>
      </li>
      <li :class="posts[2].checked ? 'checked' : ''">
        <img :src="require(`@/assets/images/${posts[2].icon}`)" :alt="posts[2].icon">
        <span>{{ posts[2].text }}</span>
      </li>
    </ul>
    <span class="total">Всего строк: {{ totalCount }}</span>

  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Data, Computed',
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
    font-size: 2rem;
  }
}
</style>
