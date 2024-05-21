<template>
  
      <div class="row col-8 techcol">
        <div class="tech m-4" id="java">
            
          <img class="icon" src="../assets/java.png" alt="" />
        </div>

        <div class="tech m-4" id="js">
          <img class="icon" src="../assets/js.png" alt="" />
        </div>

        <div class="tech m-4" id="git">
          <img class="icon" src="../assets/git.png" alt="" />
        </div>
        <div class="tech m-4" id="html">
            <img class="icon" src="../assets/html.png" alt="">


        </div>


        <div class="tech m-4" id="vue">
            <img class="icon" src="../assets/vue.png" alt="">


        </div>
        <div class="tech m-4" id="docker">
            <img class="icon" src="../assets/docker.png" alt="">


        </div>
        <div class="tech m-4" id="laravel">
            <img class="icon" src="../assets/laravel.png" alt="">


        </div>


        <div class="tech m-4" id="sql">
            <img class="icon" src="../assets/sql.png" alt="">


        </div>
        <div class="tech m-4" id="c">
            <img class="icon" src="../assets/c.png" alt="">


        </div>

        <div class="tech m-4" id="php">
            <img class="icon" src="../assets/php.png" alt="">


        </div>

        <div class="tech m-4" id="css">
            <img class="icon" src="../assets/css.png" alt="">


        </div>

        <div class="tech m-4" id="python">
            <img class="icon" src="../assets/python.png" alt="">


        </div>




    


     
  </div>
</template>
<script>
export default {
  name: "Technologies",
  data() {
    return {};
  },
  methods: {},
};
</script>
<style scoped>
.tech {
  align-items: center;
  width: auto;
  height: auto;

  /* box-shadow: 0 4px 8px 0 rgba(212, 223, 215, 0.2); */
  transition: 0.3s;
  border-radius: 8px;
  background-color: white;
}
.tech:hover {
  transform: scale(1.15);
  background-color: #090000;
  border-radius: 20px;
  
  transition: 0.5s;
}

.icon {
  width: 90px;
  height: 90px;
}
.row {
  position: relative;
  left: 20%;
}
.techcol{
  justify-content: center;
}

</style>
