<template>
  <div class="row techcol mt-5">
    <div class="tech m-4" id="java">
      <img class="icon" src="../assets/java.png" alt="" />
      <span class="tooltip">Java</span>
    </div>

    <div class="tech m-4" id="js">
      <img class="icon" src="../assets/js.png" alt="" />
      <span class="tooltip">JavaScript</span>
    </div>

    <div class="tech m-4" id="git">
      <img class="icon" src="../assets/git.png" alt="" />
      <span class="tooltip">Git</span>
    </div>
    <div class="tech m-4" id="html">
      <img class="icon" src="../assets/html.png" alt="" />
      <span class="tooltip">HTML</span>
    </div>

    <div class="tech m-4" id="vue">
      <img class="icon" src="../assets/vue.png" alt="" />
      <span class="tooltip">Vue.js</span>
    </div>
    <div class="tech m-4" id="docker">
      <img class="icon" src="../assets/docker.png" alt="" />
      <span class="tooltip">Docker</span>
    </div>
    <div class="tech m-4" id="laravel">
      <img class="icon" src="../assets/laravel.png" alt="" />
      <span class="tooltip">Laravel</span>
    </div>

    <div class="tech m-4" id="sql">
      <img class="icon" src="../assets/sql.png" alt="" />
      <span class="tooltip">SQL</span>
    </div>
    <div class="tech m-4" id="c">
      <img class="icon" src="../assets/c.png" alt="" />
      <span class="tooltip">C</span>
    </div>

    <div class="tech m-4" id="php">
      <img class="icon" src="../assets/php.png" alt="" />
      <span class="tooltip">PHP</span>
    </div>

    <div class="tech m-4" id="css">
      <img class="icon" src="../assets/css.png" alt="" />
      <span class="tooltip">CSS</span>
    </div>

    <div class="tech m-4" id="python">
      <img class="icon" src="../assets/python.png" alt="" />
      <span class="tooltip">Python</span>
    </div>
  </div>
</template>

<style scoped>
.tech {
  align-items: center;
  width: auto;
  height: auto;
  transition: 0.3s;
  border-radius: 8px;
  background-color: white;
  position: relative;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.tech:hover {
  transform: scale(1.15);
  background-color: #E0E0E0;
  border-radius: 20px;
  transition: 0.5s;
}

.icon {
  width: 90px;
  height: 90px;
}

.techcol {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.tooltip {
  visibility: hidden;
  width: 100px;
  background-color: #4ECDC4;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px;
  position: absolute;
  z-index: 1;
  bottom: 125%;
  left: 50%;
  margin-left: -50px;
  opacity: 0;
  transition: opacity 0.3s;
}

.tech:hover .tooltip {
  visibility: visible;
  opacity: 1;
}

@media (max-width: 1200px) {
  .icon {
    width: 80px;
    height: 80px;
  }
}

@media (max-width: 992px) {
  .icon {
    width: 70px;
    height: 70px;
  }

  .tech {
    margin: 2%;
  }
}

@media (max-width: 768px) {
  .icon {
    width: 60px;
    height: 60px;
  }

  .tooltip {
    width: 80px;
    margin-left: -40px;
  }
}

@media (max-width: 576px) {
  .icon {
    width: 60px;
    height: 60px;
  }

  .tech {
    margin: 5%;
  }

  .tooltip {
    width: 70px;
    margin-left: -35px;
  }
}
</style>
