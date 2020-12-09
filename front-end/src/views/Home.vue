<template>
<div class="home">
  <div class="image-gallery">
    <div class="image" v-for="item in items" :key="item.id">
      <h1>{{item.title}}</h1>
      <h2>- {{item.description}}</h2>
      <h3>~ {{item.author}}</h3>
      <img :src="item.path" />
    </div>
  </div>
</div>
</template>

<style scoped>
.image h2 {
  font-style: italic;
}

/* Masonry */
*,
*:before,
*:after {
  box-sizing: inherit;
}

.image-gallery {
  column-gap: 1.5em;
}



.image {
  margin: 10px;
  background-color: #FAE4E2;
  display: inline-block;
  width: 100%;
  border: 3px solid #fff;
  padding: 0px;
  box-shadow: 10px 10px 5px grey;
}

.image img {
  width: 200px;

}

/* Masonry on large screens */
@media only screen and (min-width: 1024px) {
  .image-gallery {
    column-count: 4;
  }
}

/* Masonry on medium-sized screens */
@media only screen and (max-width: 1023px) and (min-width: 768px) {
  .image-gallery {
    column-count: 3;
  }
}

/* Masonry on small screens */
@media only screen and (max-width: 767px) and (min-width: 540px) {
  .image-gallery {
    column-count: 2;
  }
}
</style>
<script>
// @ is an alias to /src

import axios from 'axios';
export default {
  name: 'Home',
  data() {
    return {
     items: [],
    }
  },
  created() {
    this.getItems();
  },
  methods: {
    async getItems() {
      try {
        let response = await axios.get("/api/items");
        this.items = response.data;
        return true;
      } catch (error) {
        console.log(error);
      }
    },
  }
}
</script>
