<template>
    <div>
      <div class="contenedor proyectos mt-5">
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank">Pokedex</a>
          </h2>
          <a href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank">
            <img class="proyectImg" src="../assets/pokedexpedro.gif" alt="imagenproyecto" />
          </a>
          <p :class="{'textLight': lights, 'textDark': !lights}" class="proyectDescription mt-4">{{ descriptionPokedex }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://pedrolp7.github.io/ahorcado.js/" target="_blank">{{ ahorcadoTitle }}</a>
          </h2>
          <a href="https://pedrolp7.github.io/ahorcado.js/" target="_blank">
            <img class="proyectImg" src="../assets/ahorcadopedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionAhorcado }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://pedrolp7.github.io/ahorcado.js/" target="_blank">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://pedrolp7.github.io/ahorcado.js/" target="_blank">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://pedrolp7.github.io/pomodoro/" target="_blank">Pomodoro-Kanban</a>
          </h2>
          <a href="https://pedrolp7.github.io/pomodoro/" target="_blank">
            <img class="proyectImg" src="../assets/pomodoropedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionPomodoro }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://pedrolp7.github.io/pomodoro/" target="_blank">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://pedrolp7.github.io/pomodoro/" target="_blank">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://github.com/PedroLP7/coleccionM07" target="_blank">{{ phpCollection }}</a>
          </h2>
          <a href="https://github.com/PedroLP7/coleccionM07" target="_blank">
            <img class="proyectImg" src="../assets/coleccionphppedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionCollection }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://github.com/PedroLP7/coleccionM07" target="_blank">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://github.com/PedroLP7/coleccionM07" target="_blank">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://github.com/PedroLP7/riders" target="_blank">RIDERS</a>
          </h2>
          <a href="https://github.com/PedroLP7/riders" target="_blank">
            <img class="proyectImg" src="../assets/riderspedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionRiders }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://github.com/PedroLP7/riders" target="_blank">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://github.com/PedroLP7/riders" target="_blank">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://github.com/PedroLP7/Aerolineav2" target="_blank">{{ aeroTitle }}</a>
          </h2>
          <a href="https://github.com/PedroLP7/Aerolineav2" target="_blank">
            <img class="proyectImg" src="../assets/aeropedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionAero }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://github.com/PedroLP7/Aerolineav2">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://github.com/PedroLP7/Aerolineav2">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://github.com/PedroLP7/RPGjava" target="_blank">{{ laberynthGame }}</a>
          </h2>
          <a href="https://github.com/PedroLP7/RPGjava" target="_blank">
            <img class="proyectImg" src="../assets/rpgpedro.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionLaberyinth }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://github.com/PedroLP7/RPGjava">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://github.com/PedroLP7/RPGjava">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
  
        <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
          <h2 class="proyectTitle">
            <a :class="{'textLight': lights, 'textDark': !lights}" href="https://github.com/jeansterj/laiaGame" target="_blank">{{ laiatTitle }}</a>
          </h2>
          <a href="https://github.com/jeansterj/laiaGame" target="_blank">
            <img class="proyectImg" src="../assets/LAIAPEDRO.gif" alt="imagenproyecto" />
          </a>
          <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{ descriptionLaia }}</p>
          <div id="proyectoDiv-footer">
            <p class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">
              {{ plusinfo }}
              <a v-if="lights" href="https://github.com/jeansterj/laiaGame">
                <img class="animacion" src="../assets/githubnegro.svg" alt="" />
              </a>
              <a v-if="!lights" href="https://github.com/jeansterj/laiaGame">
                <img class="animacion" src="../assets/githubclaro.svg" alt="" />
              </a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Proyects',
    props: {
      language: String,
      lights: Boolean
    },
    computed: {
      descriptionPokedex() {
        if (this.language === 'catalan') {
          return 'Aquest projecte esta fet amb vue ,  fent  cridades a la api publica de pokemon.';
        } else if (this.language === 'spanish') {
          return 'Este proyecto esta hecho en vue , haciendo llamadas a la api publica de pokemon.';
        } else if (this.language === 'english') {
          return 'This proyect is made with vue , making calls to the public pokemon api.';
        }
      },
      aeroTitle() {
        if (this.language === 'catalan') {
          return 'Aerolinea';
        } else if (this.language === 'spanish') {
          return 'Aerlinea';
        } else if (this.language === 'english') {
          return 'Airline';
        }
      },
      ahorcadoTitle() {
        if (this.language === 'catalan') {
          return 'Penjat';
        } else if (this.language === 'spanish') {
          return 'Ahorcado';
        } else if (this.language === 'english') {
          return 'Hangman';
        }
      },
      laberynthGame() {
        if (this.language === 'catalan') {
          return 'Laberint';
        } else if (this.language === 'spanish') {
          return 'Laberinto';
        } else if (this.language === 'english') {
          return 'Maze';
        }
      },
      laiatTitle() {
        if (this.language === 'catalan') {
          return 'Laia, ens ilumines';
        } else if (this.language === 'spanish') {
          return 'Laia, nos iluminas';
        } else if (this.language === 'english') {
          return 'Laia, light us up';
        }
      },
      phpCollection() {
        if (this.language === 'catalan') {
          return 'Colecció PHP';
        } else if (this.language === 'spanish') {
          return 'Coleccion PHP';
        } else if (this.language === 'english') {
          return 'PHP Collection';
        }
      },
      plusinfo() {
        if (this.language === 'catalan') {
          return 'Més informació a github';
        } else if (this.language === 'spanish') {
          return 'Más información en github';
        } else if (this.language === 'english') {
          return 'More info in github';
        }
      },
      descriptionAhorcado() {
        if (this.language === 'catalan') {
          return 'Aquest projecte esta fet amb javascript. Simula el joc del penjat.';
        } else if (this.language === 'spanish') {
          return 'Este proyecto esta hecho con javascript. Simula el juego del ahorcado.';
        } else if (this.language === 'english') {
          return 'This project is made with javascript. Simulates the hangman game.';
        }
      },
      descriptionPomodoro() {
        if (this.language === 'catalan') {
          return 'Aquest projecte esta fet amb javascript. Es una barreja de pomodoro y kanban.';
        } else if (this.language === 'spanish') {
          return 'Este proyecto esta hecho con javascript. Es una mezcla de pomodoro y kanban.';
        } else if (this.language === 'english') {
          return 'This project is made with javascript. It is a mix of pomodoro and kanban.';
        }
      },
      descriptionCollection() {
        if (this.language === 'catalan') {
          return 'Aquest projecte esta fet amb php. Interaccio basica amb una base de dades.';
        } else if (this.language === 'spanish') {
          return 'Este proyecto esta hecho con php. Interaccion basica con una base de datos.';
        } else if (this.language === 'english') {
          return 'This project is made with php. Basic interaction with a database.';
        }
      },
      descriptionRiders() {
        if (this.language === 'catalan') {
          return 'Segon proyecte de DAW , utilitza laravel per el backend y vue per el frontend.';
        } else if (this.language === 'spanish') {
          return 'Segundo proyecto de DAW , utiliza laravel para el backend y vue para el frontend.';
        } else if (this.language === 'english') {
          return 'Second project of DAW , uses laravel for the backend and vue for the frontend.';
        }
      },
      descriptionAero() {
        if (this.language === 'catalan') {
          return 'Primer proyecte utilitzant POO , Simula la gestió una aerolinea.';
        } else if (this.language === 'spanish') {
          return 'Primer proyecto utilizando POO , Simula la gestión una aerolinea.';
        } else if (this.language === 'english') {
          return 'First project using POO Simulates the management of an airline.';
        }
      },
      descriptionLaberyinth() {
        if (this.language === 'catalan') {
          return 'Proyecte utilitzant swing , una llibreria de java per fer interficies grafiques.';
        } else if (this.language === 'spanish') {
          return 'Proyecto utilizando swing , una libreria de java para hacer interfaces graficas.';
        } else if (this.language === 'english') {
          return 'Project using swing , a java library to make graphic interfaces.';
        }
      },
      descriptionLaia() {
        if (this.language === 'catalan') {
          return 'Primer proyecte de DAW, utilitzant Three.js , una llibreria de 3D en javascript.';
        } else if (this.language === 'spanish') {
          return 'Primer proyecto de DAW, utilizando Three.js , una libreria de 3D en javascript.';
        } else if (this.language === 'english') {
          return 'First project of DAW, using Three.js , a 3D library in javascript.';
        }
      }
    }
  };
  </script>
  
  <style>
  .proyectImg {
    width: 600px !important;
    height: 400px !important;
  }
  
  .contenedor {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
  }
  
  .row {
    margin-bottom: 80px;
  }
  
  .proyectoDiv img {
    width: 25px;
  }
  
  .proyectoDivLight img {
    width: 25px;
  }
  
  .proyectoDiv {
    border: solid 2px #e0e0e0;
    border-radius: 10px;
    padding: 7px;
    margin: 10px;
    height: 620px;
    box-shadow: 0 0 10px #4ecdc4;
  }
  
  .proyectoDivLight {
    border: solid 2px #261e1e;
    border-radius: 10px;
    padding: 7px;
    margin: 10px;
    height: 620px;
    border: 1px solid #4ecdc4;
    box-shadow: 0 0 10px #1a1b1b;
  }
  
  .proyectTitle {
    text-decoration: underline;
    text-underline-offset: 7px;
  }
  
  p {
    margin: 10px;
    width: 70%;
  }
  
  #proyectoDiv-footer {
    position: relative;
    top: 4%;
  }
  
  .githubtext img {
    width: 35px;
    height: 35px;
    margin-left: 7px;
    margin-bottom: 8px;
  }
  
  .githubtext img:hover {
    transform: scale(1.2);
    transition: 0.5s;
  }
  
  @keyframes aumentoDisminucion {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.3);
    }
    100% {
      transform: scale(1);
    }
  }
  
  .animacion {
    animation: aumentoDisminucion 2s infinite;
  }
  
  @media (max-width: 768px) {
    .proyectImg {
      width: 100% !important;
      height: auto !important;
    }
  
    .proyectoDiv,
    .proyectoDivLight {
      width: 100%;
      margin-bottom: 20px;
    }
  
    .proyectTitle {
      font-size: 24px;
    }
  
    .proyectDescription {
      font-size: 16px;
      width: 90%;
    }
  
    .githubtext img {
      width: 30px;
      height: 30px;
    }
  }
  </style>
  