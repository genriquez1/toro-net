<template>
  <div id="app">

       <br>
       <br>
       <br>

        <div class="container  bg-light">

                 <!-- <hr>
                <router-link to="/">Home</router-link>
                <a v-if="!this.$store.state.user.displayName" href="/register" @click="register">Register</a>
                <a v-if="this.$store.state.user.displayName" href="/logout" @click="logout">Logout</a>
                <router-link v-else to="/login">Login</router-link>
                <h1>{{ title }}</h1>
                <hr /> -->
                <router-view />


        </div>


      <div class="">
        <br>
        <br>
        <br>
        <br>
      </div>



  </div>

</template>

<script>
export default {
  name: 'app',
  // data:
  // {
  //   showContent:true,
  // },
  data () {
    return {
      title: 'Toro--Net',
    }
  },
  computed: {

  },
  methods: {
    logout() {
      this.$store.dispatch('logout')
    },
    register() {
       location.reload();
    }
  },
  mounted() {
    this.$store.dispatch('getUser')
    console.log(this.$store.state)
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

a {
  color: #42b983;
}
</style>
