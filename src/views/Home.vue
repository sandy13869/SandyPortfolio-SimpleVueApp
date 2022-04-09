<template>
  <!-- <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>  
  </div> -->
  <h1> {{title}} </h1><br>
  <input type="text" ref="name"><br><br>

  <button @click="handleClick()"> Click me </button>

</template>

<script>


// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

// export default {
//   name: 'Home',
//   components: {
//     HelloWorld
//   }
// }

export default {
  name: 'App',
  data() {
    return {
      title: 'Sandy\'s First Vue App  :)'
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    }
  }
}
</script>

<style scoped>
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
