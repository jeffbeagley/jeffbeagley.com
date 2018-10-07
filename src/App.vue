<template>
  <div id="app">
 <b-container>
        <b-jumbotron header="Bootstrap Vue"
                     lead="Bootstrap 4 Components for Vue.js 2"
        >
          <p>For more information visit our website</p>
          <b-btn variant="primary" href="https://bootstrap-vue.js.org/">More Info</b-btn>
        </b-jumbotron>

        <b-form-group horizontal
                      :label-cols="4"
                      description="Let us know your name."
                      label="Enter your name"
        >
           <b-form-input v-model.trim="name"></b-form-input>
        </b-form-group>

        <b-alert variant="success" :show="showAlert">
          Hello {{ name }}
        </b-alert>
      </b-container>
  </div>
</template>

<script>
export default {
  name: 'app',
        el: "#app",
        data: {
          name: ''
        },
        computed: {
          showAlert() {
            return this.name.length > 4 ? true : false;
          }
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
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
