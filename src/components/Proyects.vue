<template >
    <div >

       <!-- <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='catalan'"> proyectes en catala</p>
         <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='spanish'"> proyectes en spanish</p>
            <p :class="{'textLight': lights, 'textDark': !lights}" v-if="language==='english'"> proyectes en english</p>  -->

        <div class="contenedor proyectos ">

          

            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                <h2 :class="{'textLight': lights, 'textDark': !lights}" class="proyectTitle">Pokedex</h2>
                 <img class="proyectImg" src="../assets/pokedexpedro.gif" alt="imagenproyecto">
                 <p   :class="{'textLight': lights, 'textDark': !lights}" class="proyectDescription mt-4">{{   descriptionPokedex}}</p>
                 <div id="proyectoDiv-footer">
                    <p class="githubtext":class="{'textLight': lights, 'textDark': !lights}">{{ plusinfo }}
                        <a v-if="lights" href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank"> <img  src="../assets/githubnegro.svg" alt=""></a>
                    <a v-if="!lights" href="https://pedrolp7.github.io/Pokedex-VUE/" target="_blank"><img  src="../assets/githubclaro.svg" alt=""></a>
                    
                    </p>
                </div>
                
            
            </div>
            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}" >
                <h2 class="proyectTitle " :class="{'textLight': lights, 'textDark': !lights}">{{ ahorcadoTitle }}</h2>
                 <img class="proyectImg" src="../assets/ahorcadopedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionAhorcado}}</p>

                 <div id="proyectoDiv-footer">
                    <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}"> {{ plusinfo }} <a v-if="lights" href="https://pedrolp7.github.io/ahorcado.js/" target="_blank"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://pedrolp7.github.io/ahorcado.js/" target="_blank"><img  src="../assets/githubclaro.svg" alt=""></a></p>

                 </div>
                
                 
            
            </div>




            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">Pomodoro</h2>
                 <img class="proyectImg" src="../assets/pomodoropedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionPomodoro}}</p>
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">{{ plusinfo }}  <a v-if="lights" href="https://pedrolp7.github.io/pomodoro/" target="_blank"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://pedrolp7.github.io/pomodoro/" target="_blank"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                  
            
            </div>
            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">{{phpCollection}}</h2>
                 <img class="proyectImg" src="../assets/coleccionphppedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionCollection}}</p>
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}"> {{plusinfo}} <a v-if="lights" href="https://github.com/PedroLP7/coleccionM07" target="_blank"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://github.com/PedroLP7/coleccionM07" target="_blank"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                 
            
            </div>

            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">RIDERS </h2>
                 <img class="proyectImg" src="../assets/riderspedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4 " :class="{'textLight': lights, 'textDark': !lights}">{{descriptionRiders}}</p>
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">{{ plusinfo }} <a v-if="lights" href="https://github.com/PedroLP7/riders" target="_blank"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://github.com/PedroLP7/riders" target="_blank"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                 
            
            </div>
            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">{{ aeroTitle }}</h2>  
                 <img class="proyectImg" src="../assets/aeropedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionAero}} </p> 
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}"> {{ plusinfo }}  <a v-if="lights" href="https://github.com/PedroLP7/Aerolineav2"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://github.com/PedroLP7/Aerolineav2"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                
            
            </div>

            <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}">
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">{{ laberynthGame }}</h2>
                 <img class="proyectImg" src="../assets/rpgpedro.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionLaberyinth}}</p>
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}">{{ plusinfo }}  <a v-if="lights" href="https://github.com/PedroLP7/RPGjava"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://github.com/PedroLP7/RPGjava"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                
                </div>


                <div :class="{'proyectoDivLight': lights, 'proyectoDiv': !lights}" >
                <h2 class="proyectTitle" :class="{'textLight': lights, 'textDark': !lights}">{{ laiatTitle}}</h2>
                 <img class="proyectImg" src="../assets/LAIAPEDRO.gif" alt="imagenproyecto">
                 <p class="proyectDescription mt-4" :class="{'textLight': lights, 'textDark': !lights}">{{descriptionLaia}}</p>
                 <p  class="githubtext" :class="{'textLight': lights, 'textDark': !lights}"> {{ plusinfo }} <a v-if="lights" href="https://github.com/jeansterj/laiaGame"> <img  src="../assets/githubnegro.svg" alt=""></a>
                   <a v-if="!lights" href="https://github.com/jeansterj/laiaGame"><img  src="../assets/githubclaro.svg" alt=""></a></p>
                 
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
        descriptionPokedex(){
            if(this.language === 'catalan'){
                return 'Aquest projecte esta fet amb vue ,  fent  cridades a la api publica de pokemon.';
            }else if(this.language === 'spanish'){
                return 'Este proyecto esta hecho en vue , haciendo llamadas a la api publica de pokemon.';
            }else if(this.language === 'english'){
                return 'This proyect is made with vue , making calls to the public pokemon api.' ;
            }
        },
                aeroTitle(){
                    if(this.language === 'catalan'){
                        return 'Aerolinea';
                    }else if(this.language === 'spanish'){
                        return 'Aerlinea';
                    }else if(this.language === 'english'){
                        return 'Airline';
                    }
                },
                ahorcadoTitle(){
                    if(this.language === 'catalan'){
                        return 'Penjat';
                    }else if(this.language === 'spanish'){
                        return 'Ahorcado';
                    }else if(this.language === 'english'){
                        return 'Hangman';
                    }
                },
                laberynthGame(){
                    if(this.language === 'catalan'){
                        return 'Laberint';
                    }else if(this.language === 'spanish'){
                        return 'Laberinto';
                    }else if(this.language === 'english'){
                        return 'Maze';
                    }
                },
                laiatTitle(){
                    if(this.language === 'catalan'){
                        return 'Laia, ens ilumines';
                    }else if(this.language === 'spanish'){
                        return 'Laia, nos iluminas';
                    }else if(this.language === 'english'){
                        return 'Laia, light us up';
                    }
                },
                phpCollection(){
                    if(this.language === 'catalan'){
                        return 'Colecció PHP';
                    }else if(this.language === 'spanish'){
                        return 'Coleccion PHP';
                    }else if(this.language === 'english'){
                        return 'PHP Collection';
                    }
                },
                plusinfo(){
                    if(this.language === 'catalan'){
                        return 'Més informació a github';
                    }else if(this.language === 'spanish'){
                        return 'Más información en github';
                    }else if(this.language === 'english'){
                        return 'More info in github';
                    }
                },
                descriptionAhorcado(){
                    if(this.language === 'catalan'){
                        return 'Aquest projecte esta fet amb javascript. Simula el joc del penjat.     ';
                    }else if(this.language === 'spanish'){
                        return 'Este proyecto esta hecho con javascript. Simula el juego del ahorcado.';
                    }else if(this.language === 'english'){
                        return 'This project is made with javascript. Simulates the hangman game.' ;
                    }
                },
                descriptionPomodoro(){
                    if(this.language === 'catalan'){
                        return 'Aquest projecte esta fet amb javascript. Es una barreja de pomodoro y kanban.';
                    }else if(this.language === 'spanish'){
                        return 'Este proyecto esta hecho con javascript. Es una mezcla de pomodoro y kanban.';
                    }else if(this.language === 'english'){
                        return 'This project is made with javascript. It is a mix of pomodoro and kanban.' ;
                    }
                },
                descriptionCollection(){
                    if(this.language === 'catalan'){
                        return 'Aquest projecte esta fet amb php. Interaccio basica amb una base de dades.';
                    }else if(this.language === 'spanish'){
                        return 'Este proyecto esta hecho con php. Interaccion basica con una base de datos.';
                    }else if(this.language === 'english'){
                        return 'This project is made with php. Basic interaction with a database.' ;
                    }
                },
                descriptionRiders(){
                    if(this.language === 'catalan'){
                        return 'Segon proyecte de DAW , utilitza laravel per el backend y vue per el frontend.';
                    }else if(this.language === 'spanish'){
                        return 'Segundo proyecto de DAW , utiliza laravel para el backend y vue para el frontend.';
                    }else if(this.language === 'english'){
                        return 'Second project of DAW , uses laravel for the backend and vue for the frontend.' ;
                    }
                }  ,
                descriptionAero(){
                    if(this.language === 'catalan'){
                        return 'Primer proyecte utilitzant Programació orientada a objectes , en Java.';
                    }else if(this.language === 'spanish'){
                        return 'Primer proyecto utilizando Programación orientada a objetos , en Java.';
                    }else if(this.language === 'english'){
                        return 'First project using Object Oriented Programming , in Java.' ;
                    }
                } ,
                descriptionLaberyinth(){
                    if(this.language === 'catalan'){
                        return 'Proyecte utilitzant swing , una llibreria de java per fer interficies grafiques.';
                    }else if(this.language === 'spanish'){
                        return 'Proyecto utilizando swing , una libreria de java para hacer interfaces graficas.';
                    }else if(this.language === 'english'){
                        return 'Project using swing , a java library to make graphic interfaces.' ;
                    }
                },
                descriptionLaia(){
                    if(this.language === 'catalan'){
                        return 'Primer proyecte de DAW, utilitzant Three.js , una llibreria de 3D en javascript.';
                    }else if(this.language === 'spanish'){
                        return 'Primer proyecto de DAW, utilizando Three.js , una libreria de 3D en javascript.';
                    }else if(this.language === 'english'){
                        return 'First project of DAW, using Three.js , a 3D library in javascript.' ;
                    }
                }

            
        }
}
</script>
<style>
.proyectImg{
   width: 600px!important;
   height: 400px!important;
    
    
    
}
.contenedor{
    display: flex;
    flex-wrap: wrap; 
    justify-content: space-around;
    align-items: center;
    
    
}
.row{
    margin-bottom: 80px;
}
    
  
 
    .proyectoDiv img{
        width: 25px;
       
    }
    .proyectoDivLight img{
        width: 25px;
       
    }
    .proyectoDiv{ 
        border:solid 2px #E0E0E0;
        border-radius: 10px ;
        padding: 7px;
        margin: 10px;
        height: 620px;

      
       }
       .proyectoDivLight{
        border:solid 2px #261e1e;
        border-radius: 10px ;
        padding: 7px;
        margin: 10px;
        height: 620px;


       }
       .proyectTitle{
        text-decoration: underline;
        text-underline-offset: 7px; 
       }

       p{
        margin: 10px;
        width: 70%;
       }

#proyectoDiv-footer {
    position: relative;
    top: 4%;
}

.githubtext img{
    width: 35px;
    height: 35px;
    margin-left: 1px;
   
  
   
    

}

.githubtext img:hover{
    
    transform: scale(1.2);
    transition: 0.5s;
}
      
       



</style>