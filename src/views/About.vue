<template>  
  <!-- <Model header="We are working on it..."/> -->
  <!-- <Model :header="['sam', 34, 'Group']"/> -->
  <h1> {{title}} </h1>
  <p>Welcome....</p>
  <div v-if="showModel">
    <!-- <Model :header="header" :text="title" theme="sale" @close="toggleModel"/> -->
    <Model :header="header" @close="toggleModel">
      <template v-slot:links>
        <a href="#"> SignUp </a>
        <a href="#"> Login </a>
      </template>
      <h1>Book Heading</h1>
      <p>The description of the book!</p>
    </Model>
  </div>  
  <button @click="toggleModel"> Open Model </button>
  <!-- <button @click="toggleModel"> Open Model </button> -->
</template>
<script>
import Model from '@/components/Model.vue'

export default {
  name: 'App',
  components: { Model },
  data() {
    return {
      title: 'My Rules, My wish...',
      header: 'It\'s my plan !!!',
      text: 'My Value',
      theme: 'Get What you want',
      showModel: false,
    }
  },

  methods: {
    toggleModel() {
      this.showModel = !this.showModel
    }
  }
}

</script>