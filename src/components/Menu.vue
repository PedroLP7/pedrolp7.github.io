<template>
  <div>
    
      
    
    <div class="position-absolute top-0 end-0">
      <button :class="{'buttonsActive':language=='english'}" class="btn btn-primary m-2 buttonsColorLightMode    " @click="changeLanguage('english')">
        ENG
      </button>
      <button :class="{'buttonsActive':language=='spanish'}" class="btn btn-primary m-2 buttonsColorLightMode  " @click="changeLanguage('spanish')">
        ESP
      </button>
      <button :class="{'buttonsActive':language=='catalan'}" class="btn btn-primary m-2 buttonsColorLightMode   " @click="changeLanguage('catalan')">
        CAT
      </button>
    </div>

    <div class="container mt-3">
    

      

      

      <div class="row ">
        <div id="titles">
         
 
    <button :class="{ 'activeHome': showHomeActive }"  id="homeButton" class=" btn btn-primary m-5" @click="showHome()">
        <img src="../assets/home.svg" alt="" />
      </button>
  
        <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights}"  @click="showItem1()" class="menuLightMode m-5 menu ">{{aboutMe}}</span>
        <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights}"  @click="showItem2()" class="menuLightMode m-5 ">{{proyects}}</span>
        <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights}" @click="showTech()" class="menuLightMode m-5 ">{{technologies}}</span>
        <!-- <span :class="{'active':showSkills}"  @click="showSk()" class="menu m-5">{{skills}}</span> -->
      </div>
      
        <div class="mt-1  " 
          v-if="
            !showTechnologies && !showSkills && !showProyects && !showKnow
          "
          id="presentacion"
        >
          <img  class="m-3" id="fotop" src="../assets/plp.png" alt="" />
          <!-- <span class="text-center" id="main"> {{ presentation }} </span> -->
          <p id="inicial" :class="{'textLight': lights, 'textDark': !lights}">
            <span id="" :class="{'textLight': lights, 'textDark': !lights}">{{ PedroLopez }}</span>
            <br>
            {{Textoinicial}}
          </p>
         
        </div>
        <Know v-if="showKnow" :language="language" :lights="lights" />
        <Technologies v-if="showTechnologies" />
        <Skills v-if="showSkills" />
        <Proyects v-if="showProyects" :language="language" :lights="lights" />
      </div>

      <footer class="footer mt-3 iconsFooter">
        <a href="https://github.com/PedroLP7?tab=repositories" target="_blank">
          <img class="m-2 " src="../assets/github.svg" alt="github_icon" />
        </a>
        <!-- <a href="mailto:plopezp2223@politecnics.barcelona"></a> -->
        <img
          @click="showMail()"
          class="m-2 "
          src="../assets/mail.svg"
          alt="mail_icon"
        />
        <span v-if="showM"> pedro.7.1995@live.com</span>

        <a
          href="https://www.linkedin.com/in/pedro-lopez-81b8012b3/"
          target="_blank"
          ><img class="m-2 iconsmi" src="../assets/linkedin.svg" alt="linkedin_icon"
        /></a>

        <img
          @click="showTlf()"
          class="m-2 "
          src="../assets/phone.svg"
          alt="phone_icon"
        />
        <span v-if="showPhone">664688976</span>

        <a href="PLCV.pdf" download="pedroLp_cv.pdf"><img class="m-2" src="../assets/cv.svg" alt="cv_icon"></a>
        <button id="light" @click="manageLight(lights)" class="btn btn-secondary"> <img v-if="!lights" src="../assets/lightbulb.svg"  alt="light"> <img v-else src="../assets/lightbulbup.svg" alt="light" /></button>

      </footer>
    </div>
  </div>
</template>
<script>
import Know from "./Know.vue";
import Technologies from "./Technologies.vue";
import Skills from "./Skills.vue";
import Proyects  from "./Proyects.vue";


export default {
  components: {
    Know,
    Technologies,
    Skills,
    Proyects
  },
  computed: {
    presentation() {
      return this.language === "english"
        ? "Pedro Lopez , Web Developer"
        : this.language === "spanish"
        ? "Pedro Lopez , desarrollador web"
        : this.language === "catalan"
        ? "Pedro Lopez , desenvolupador web "
        : "PRESENTATION IN ENGLISH";
    },
    aboutMe() {
      return this.language === "english"
        ? "ABOUT ME"
        : this.language === "spanish"
        ? "SOBRE MI"
        : this.language === "catalan"
        ? "CONEIX-ME"
        : "ABOUT ME";
    },
    proyects() {
      return this.language === "english"
        ? "PROJECTS"
        : this.language === "spanish"
        ? "PROYECTOS"
        : this.language === "catalan"
        ? "PROJECTES"
        : "PROJECTS";
    },
    technologies() {
      return this.language === "english"
        ? "TECHNOLOGIES"
        : this.language === "spanish"
        ? "TECNOLOGIAS"
        : this.language === "catalan"
        ? "TECNOLOGIES"
        : "TECHNOLOGIES";
    },
    skills() {
      return this.language === "english"
        ? "SKILLS"
        : this.language === "spanish"
        ? "HABILIDADES"
        : this.language === "catalan"
        ? "HABILITATS"
        : "SKILLS";
    },
    Textoinicial(){
      return this.language === "english" 
        ? " WELCOME TO MY PORTFOLIO ,  HERE YOU CAN FIND MORE ABOUT ME"
        : this.language === "spanish"
        ? "TEXTO EN ESPAÑOL"
        : this.language === "catalan"
        ? "TEXTO EN CATALAN"
        : "TECHNOLOGIES";
      
       
    },
    PedroLopez(){
      return this.language === "english"
        ? "HELLO IM PEDRO LOPEZ "
        : this.language === "spanish"
        ? "HOLA SOY PEDRO LOPEZ"
        : this.language === "catalan"
        ? "HOLA SÓC PEDRO LOPEZ"
        : "TECHNOLOGIES";
    },
  },
  name: "Menu",

  methods: {
    showItem1() {
      this.showKnow = true;
      console.log(this.showKnow);

      this.showTechnologies = false;
      this.showSkills = false;
        this.showHomeActive = false;
        this.showProyects = false;
    },
    showItem2() {
      
      this.showProyects =true;
      this.showKnow = false;
      this.showTechnologies = false;
      this.showSkills = false;
      this.showHomeActive = false;
   
     },
    showTech() {
      this.showTechnologies = true;
      this.showKnow = false;
      this.showSkills = false;
      this.showHomeActive = false;
      this.showProyects = false;
      console.log("tecnolocias" + this.showTechnologies);
    },
    showHome() {
      this.showKnow = false;
      this.showTechnologies = false;
      this.showSkills = false;
      this.showMenuProyects = false;
      this.showProyects = false;
      this.showHomeActive = true; 
      console.log(this.showHomeActive)
     
    },
    showSk() {
      this.showSkills = true;
      this.showKnow = false;
      this.showMenuProyects = false;
      this.showTechnologies = false;
    },
    changeLanguage(language) {
      this.language = language;
      console.log(this.language);
      
    },
    showTlf() {
      if (this.showPhone) {
        this.showPhone = false;
      } else {
        this.showPhone = true;
      }
    },
    showMail() {
      if (this.showM) {
        this.showM = false;
      } else {
        this.showM = true;
      }
    },

    
    manageLight(lights){
      

      if(this.lights){
        this.lights = false;
        document.body.style.backgroundColor = "#1E1E1E";
        console.log("apagamos las luces");
       
       
      }else{
        this.lights = true;
       
        

        document.body.style.backgroundColor = "#F5F5F5";
        console.log("encendemos las luces");
       
       
       
      }
      
    }
  },
  data() {
    return {
      showKnow: false,
      showMenuProyects: false,

      showTechnologies: false,
      showSkills: false,
      language: "english",
      showPhone: false,
      showM: false,
      showHomeActive: false,
      lights: true,
      showProyects: false,
    };
  },
  beforeMount() {
    // window.addEventListener("load", function () {
    //     document.body.style.backgroundColor = "#1E1E1E";
    //   });
  },
};
</script>
<style >


  /*
  Primario: #1E1E1E (Negro)
Secundario: #272727 (Gris Oscuro)
Resaltado: #FFD700 (Amarillo Dorado)
Acento: #4ECDC4 (Verde Agua)
Texto: #FFFFFF (Blanco)
Modo Claro:

Primario: #F5F5F5 (Gris Claro)
Secundario: #E0E0E0 (Gris)
Resaltado: #FFA500 (Naranja)
Acento: #3F51B5 (Azul Índigo)
Texto: #333333 (Gris Oscuro)

*/ 
*{
  color: #130101;
  font-family: "Kanit", sans-serif;
}

.footer {
    background-color: #272727 ;
    color: #130101;
    padding: 7px 0;
    text-align: center;
    position : fixed;
    top  :90%;
    width: 100%;
    left: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 4px;
  }
   
  .buttonsColorLightMode{
    background-color: #4ECDC4 !important;
    border: none !important;
  }
  .buttonsColorLightMode:hover{
    /* background-color: #FFD700; */
    transform: scale(1.2);
    
  }
  .buttonsActive{
     color: #130101;
  text-decoration: underline !important;
  text-underline-offset: 0.2em !important;

  }

  .menuLightMode{
    font-size: 40px;
    font-weight: 500;
   
    cursor: pointer;
    user-select: none;

  }

  .menuDarkMode{
    color: #f3f4f5;
    font-size: 40px;
    font-weight: 500;
   
    cursor: pointer;
    user-select: none;

  }
  .iconsFooter img{
    width: 25px;
    height: 25px;
  }
  .textoOscuro{
    color: #130101;

  }
  .textoClaro{
    color: #f3f4f5;
  }
  .menuDarkMode:hover{
    color: transparent;
      cursor: pointer;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      -webkit-text-stroke: 1px #f3f4f5 !important;
  
   }

   .menuLightMode:hover{
    color: transparent;
      cursor: pointer;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      -webkit-text-stroke: 1px #130101;
  
   }
   #light{
    /* posicion para el boton de la luz */
      position: fixed;
      left: 95%;
   }
   

    #light img{
      width: 30px;
      height: 30px;
    }
    .textDark{
       color: #f3f4f5 ;
       
      
    }
    .textLight{
      color: #130101;
    }
    #homeButton{
      position: relative;
      left: -40px;
    }
      
  
 
</style>
