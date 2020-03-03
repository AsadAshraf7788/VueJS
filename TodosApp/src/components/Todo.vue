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
                <div class="input-group">
                  <input class="form-control  form-control-lg mt-3 " type="text" placeholder="type to add...">
                </div>
              </div>
              <button type="button" class="btn btn-light btn-outline-primary mt-3 btn-sm">Add Task</button>
              <ul class="list-group mt-4"></ul>
            </div>
          </div>
          </div>
        </div>
        </div>
      </div>
</template>

<script>
export default {
  
}
</script>

<style lang="stylus" scoped>

</style>