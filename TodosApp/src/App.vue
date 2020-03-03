<template>
  <div class="container">
    <div class="row">
      <div class="col s12">
        <div id="main" class="card  shadow-lg p-4 mb-4 bg-white ">
          <div class="card" id="nested-card">
            <div class="card-header text-center p-3 ">
              <h2>Task List Project</h2>
            </div>
            <div class="card-body">
                <div id='error'></div>
              <div class="form-group">
                <div class="alert alert-danger" v-if="error_prompt">
                  <p class="alert-dark pt-2">Please enter a task...</p>
                </div>
                <div class="input-group">
                  <input class="form-control  form-control-lg mt-3 " type="text" placeholder="type to add..." v-model="input">
                </div>
              </div>
              <button type="button" class="btn btn-light btn-outline-primary mt-3 btn-sm" v-on:click="addElement">Add Task</button>
              <ul class="list-group mt-4">
                <li v-for="todo in todos" :key="todo" class="list-group-item list-group-item-success mt-2">
                  {{todo}} 
                  <button class="btn float-right" v-on:click="deleteElement(todos.indexOf(todo))">x</button>
                </li>
              </ul>
            </div>
          </div>
          </div>
        </div>
        </div>
      </div>
</template>
<script>
// import testComponent from './components/test'
// import VM from './components/CompvModel';
// import todo from './components/Todo'
export default {
  name: 'App',
  data () {
    return {
      error_prompt : false, // Bool varibale to show error prompt
      input : '', // Variable to reactively bind Input field of app
      todos : ['Learn GIT','Lean Something New in VueJS','Sleep tight :P']
    }
  },
  methods: {
    addElement () {
      if(this.input === ''){
        this.error_prompt = true
        setTimeout(()=>this.error_prompt = false,2000);
      }else {
        this.todos.push(this.input);
      }
    },

    deleteElement (ind) {
      this.todos.splice(ind,1);
    }
  },
  components: {
    // testComponent,
    // VM,
    // todo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
