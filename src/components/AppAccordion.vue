<template>
  <div class="mt-5">
  <div class="margin container w-50 ">
    <div class="accordion" id="accordionExample">
      <div v-for="(post, i) in posts" :key="post.id" class="accordion-item">
        <h2 class="accordion-header" :id="`heading${post.id}`">
          <button
            class="accordion-button"
            :class="{ collapsed: i > 0 }"
            type="button"
            data-bs-toggle="collapse"
            :data-bs-target="`#collapse${post.id}`"
            :aria-expanded="i === 0"
            :aria-controls="`collapse${post.id}`"
          >
            {{ post.title }}
          </button>
        </h2>
        <div
          :id="`collapse${post.id}`"
          class="accordion-collapse collapse"
          :class="{ show: i === 0 }"
          :aria-labelledby="`heading${post.id}`"
          data-bs-parent="#accordionExample"
        >
          <div class="accordion-body"> {{ post.description }}</div>
        </div>
      </div>

    </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      posts: []
    }
  },
  created() {
    this.getData()
  },
  methods: {
    async getData() {
      const response = await axios.get('http://dev3.elemental.co.za/elemental-cms/front_end/get_knowledge')
      this.posts = response.data.results.sort()
      console.log(this.posts)
    }
  }
}
</script>
<style>
.margin{
  margin: 100px;
  
}
</style>