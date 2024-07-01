<template>

<div>
    <h2>Список курсов</h2>
    <div class="card1">
    <div class="card" v-for="card in cards" :key="card.id" :class="{ 'inactive': !card.isActive }">
      <h2>{{ card.isActive ? card.title : 'Кажется, курс уже не существует...' }}</h2>
      <p v-if="card.isActive">{{ card.description }}</p>
      <p v-if="card.isActive">Длительность курса: {{ card.length }}</p>
    </div>
  </div>
</div>

</template>
<script setup>
import { ref } from "vue"

const cards = ref([
{
id: 1,
title: 'Python-разработчик',
description: 'Описание: На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: true,

},
{
id: 2,
title: 'Графический дизайнер',
description: 'Описание: Научим делать бренды узнаваемыми через создание логотипов, графики для рекламы, упаковки и не только.',
length: '6 месяцев',
isActive: true,
},
{
id: 3,
title: 'Веб-разработчик',
description: 'Описание: Веб-разработчик создает сайты, сервисы и приложения, которыми мы ежедневно пользуемся.',
length: '7 месяцев',
isActive: true
},
{
id: 4,
title: 'Инженер по тестированию',
description: 'Описание: вы научитесь находить ошибки в работе сайтов и приложений с помощью Java, JavaScript или Python.',
length: '7 месяцев',
isActive: true
},
{
id: 5,
title: 'Python-разработчик',
description: 'На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: false
},
{
id: 6,
title: 'Python-разработчик',
description: 'На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: false
},
{
id: 7,
title: 'Python-разработчик',
description: 'На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: false
},
{
id: 8,
title: 'Python-разработчик',
description: 'На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: false
},
{
id: 9,
title: 'Python-разработчик',
description: 'На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Youtube написаны на Python',
length: '10 месяцев',
isActive: false
}

])
</script>
<style scoped>
.inactive {
  color: pink;
}
.card1 {
display: flex;
flex-wrap: wrap;
justify-content: space-between;
}
.card {
width: 400px;
padding: 24px 24px 16px;
background-color: #f0ebeb;
border-radius: 16px;
margin: 0 0 16px
}


.card-title {
font-size: 18px;
font-weight: 600;
margin-bottom: 8px;
}



.card-description {
color: rgb(106, 109, 114);
margin-bottom: 16px;
}

.card-length {
color: rgb(106, 109, 114);
margin-bottom: 16px;
}



.card-completed {
display: flex;
align-items: center;
gap: 4px;
}


.card-is-completed {
padding: 0 6px;
border: 1px solid rgb(42, 182, 231);
color: rgb(42, 182, 231);
border-radius: 4px;
}


.card-is-not-completed {
padding: 0 6px;
border: 1px solid rgb(166, 182, 197);
color: rgb(166, 182, 197);
border-radius: 4px;
}
</style>
