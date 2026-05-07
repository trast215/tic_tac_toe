<template>
  <div id="app">
    <div class="container">
      <div class="row my-2">
        <div class="col-12">
          <div class="w-100 d-flex justify-content-center">
            <div class="alert alert-success" role="alert">
              Player {{ Player }} wins! Click 'Reset' to restart
            </div>
          </div>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-12">
          <h2>tic tac toe</h2>
        </div>
        <div class="col-12 mt-3">
          <div class="w-100 d-flex justify-content-center">
            <div class="board_container">
              <div class="row">
                <div v-for="(button,indexs) in buttons" :key="'btn'+indexs" class="col-4 border m-0 p-0">
                  <div class="w-100 h-100 d-flex align-items-center justify-content-center cell">
                      {{ button }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row my-3">
        <div class="col-12">
          <div class="btn btn-primary">
            Reset
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      row: 3,
      buttons: 9,
      status: 'Next player: X'
    };
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

.board_container{
  width: 300px;
}
.col-4{
  height: 100px;
}
.cell:hover{
  background: #cccccc;
}
</style>