<template>
  <div>
    <div class="position-absolute top-0 end-0">
      <button :class="{'buttonsActive':language=='english'}" class="btn btn-primary m-2 buttonsColorLightMode" @click="changeLanguage('english')">
        ENG
      </button>
      <button :class="{'buttonsActive':language=='spanish'}" class="btn btn-primary m-2 buttonsColorLightMode" @click="changeLanguage('spanish')">
        ESP
      </button>
      <button :class="{'buttonsActive':language=='catalan'}" class="btn btn-primary m-2 buttonsColorLightMode" @click="changeLanguage('catalan')">
        CAT
      </button>
    </div>

    <div class="container mt-5">
      <div class="row">
        <div id="titles" class="mt-3 text-center text-md-start">
          <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights, 'activeText' : showHomeActive}" @click="showHome()" class="menuLightMode m-2 m-md-5">HOME</span>
          <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights, 'activeText' : showKnow}" @click="showItem1()" class="menuLightMode m-2 m-md-5">{{ aboutMe }}</span>
          <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights, 'activeText' : showProyects}" @click="showItem2()" class="menuLightMode m-2 m-md-5">{{ proyects }}</span>
          <span :class="{'menuLightMode': lights, 'menuDarkMode': !lights, 'activeText' : showTechnologies}" @click="showTech()" class="menuLightMode m-2 m-md-5">{{ technologies }}</span>
        </div>
        
        <div class="mt-5 text-center text-md-start" v-if="!showTechnologies && !showSkills && !showProyects && !showKnow" id="presentacion">
          <img class="m-3 img-fluid" id="fotoPersonal" src="../assets/plp.jpg" alt="" />
          <p id="inicial" :class="{'textLight': lights, 'textDark': !lights}">
            <span class="Presentation" :class="{'textLight': lights, 'textDark': !lights}">{{ PedroLopez }}</span>
            <br>
            <span @click="showItem1()" class="underlineText" :class="{'textLight': lights, 'textDark': !lights}">{{ Textoinicial }}</span>
          </p>
          <br><br>
          <p class="helloWorld animated-text" @click="showItem2()">{{ helloWorld }}</p>
          <div class="d-flex justify-content-center justify-content-md-end">
            <img id="imgprincipal" src="../assets/prog.jpg" alt="" class="img-fluid img-principal" />
          </div>
        </div>

        <Know v-if="showKnow" :language="language" :lights="lights" />
        <Technologies v-if="showTechnologies" />
        <Skills v-if="showSkills" />
        <Proyects v-if="showProyects" :language="language" :lights="lights" />
      </div>

      <footer class="footer mt-3 iconsFooter">
        <a href="https://github.com/PedroLP7?tab=repositories" target="_blank">
          <img class="m-2" src="../assets/github.svg" alt="github_icon" />
        </a>
        <img @click="showMail()" class="m-2" src="../assets/mail.svg" alt="mail_icon" />
        <span v-if="showM"><a class="textDark" href="mailto:plopezp2223@politecnics.barcelona">pedro.7.1995@live.com</a></span>
        <a href="https://www.linkedin.com/in/pedro-lopez-81b8012b3/" target="_blank">
          <img class="m-2 iconsmi" src="../assets/linkedin.svg" alt="linkedin_icon" />
        </a>
        <img @click="showTlf()" class="m-2" src="../assets/phone.svg" alt="phone_icon" />
        <span class="textDark" v-if="showPhone">664688976</span>
        <a href="PLCV.pdf" download="pedroLp_cv.pdf"><img class="m-2" src="../assets/cv.svg" alt="cv_icon"></a>
        <button id="light" @click="manageLight(lights)" class="btn btn-secondary">
          <img v-if="!lights" src="../assets/lightbulb.svg" alt="light">
          <img v-else src="../assets/lightbulbup.svg" alt="light" />
        </button>
      </footer>
    </div>
  </div>
</template>

<script>
import Know from "./Know.vue";
import Technologies from "./Technologies.vue";
import Skills from "./Skills.vue";
import Proyects from "./Proyects.vue";

export default {
  components: {
    Know,
    Technologies,
    Skills,
    Proyects,
  },
  computed: {
    aboutMe() {
      return this.language === "english" ? "ABOUT ME" : this.language === "spanish" ? "SOBRE MI" : this.language === "catalan" ? "CONEIX-ME" : "ABOUT ME";
    },
    proyects() {
      return this.language === "english" ? "PROJECTS" : this.language === "spanish" ? "PROYECTOS" : this.language === "catalan" ? "PROJECTES" : "PROJECTS";
    },
    technologies() {
      return this.language === "english" ? "TECHNOLOGIES" : this.language === "spanish" ? "TECNOLOGIAS" : this.language === "catalan" ? "TECNOLOGIES" : "TECHNOLOGIES";
    },
    skills() {
      return this.language === "english" ? "SKILLS" : this.language === "spanish" ? "HABILIDADES" : this.language === "catalan" ? "HABILITATS" : "SKILLS";
    },
    Textoinicial() {
      return this.language === "english" ? "WELCOME TO MY PORTFOLIO, HERE YOU CAN KNOW MORE ABOUT ME" : this.language === "spanish" ? "BIENVENIDO A MI PORTAFOLIO, AQUI PUEDES CONOCERME MAS" : this.language === "catalan" ? "BENVINGUT AL MEU PORTFOLI, AQUI POTS CONEIXER-ME MES" : "WELCOME TO MY PORTFOLIO, HERE YOU CAN KNOW MORE ABOUT ME";
    },
    PedroLopez() {
      return this.language === "english" ? "PEDRO LOPEZ, WEB DEVELOPER" : this.language === "spanish" ? "PEDRO LOPEZ, DESARROLLADOR WEB" : this.language === "catalan" ? "PEDRO LOPEZ, DESENVOLUPADOR WEB" : "PEDRO LOPEZ, WEB DEVELOPER";
    },
    helloWorld() {
      return this.language === "english" ? "{{ HELLO WORLD ! }}" : this.language === "spanish" ? "{{ HOLA MUNDO ! }}" : this.language === "catalan" ? "{{ HOLA MÓN ! }}" : "{{ HELLO WORLD ! }}";
    },
  },
  name: "Menu",
  methods: {
    showItem1() {
      this.showKnow = true;
      this.showTechnologies = false;
      this.showSkills = false;
      this.showHomeActive = false;
      this.showProyects = false;
    },
    showItem2() {
      this.showProyects = true;
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
    },
    showHome() {
      this.showKnow = false;
      this.showTechnologies = false;
      this.showSkills = false;
      this.showMenuProyects = false;
      this.showProyects = false;
      this.showHomeActive = true;
    },
    showSk() {
      this.showSkills = true;
      this.showKnow = false;
      this.showMenuProyects = false;
      this.showTechnologies = false;
    },
    changeLanguage(language) {
      this.language = language;
    },
    showTlf() {
      this.showPhone = !this.showPhone;
    },
    showMail() {
      this.showM = !this.showM;
    },
    manageLight(lights) {
      this.lights = !this.lights;
      document.body.style.backgroundColor = this.lights ? "#F5F5F5" : "#1E1E1E";
    },
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
      showHomeActive: true,
      lights: false,
      showProyects: false,
    };
  },
  beforeMount() {
    window.addEventListener("load", function () {
      document.body.style.backgroundColor = "#1E1E1E";
    });
  },
};
</script>

<style>
* {
  color: #130101;
  font-family: "Kanit", sans-serif;
}

.footer {
  background-color: #272727;
  color: #130101;
  padding: 7px 0;
  text-align: center;
  position: fixed;
  top: 90%;
  width: 100%;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 4px;
}

.buttonsColorLightMode {
  background-color: #4ecdc4 !important;
  border: none !important;
}

.buttonsColorLightMode:hover {
  transform: scale(1.2);
}

.buttonsActive {
  color: #130101;
  text-decoration: underline !important;
  text-underline-offset: 0.2em !important;
}

.menuLightMode {
  font-size: 40px;
  font-weight: 500;
  cursor: pointer;
  user-select: none;
}

.menuDarkMode {
  color: #f3f4f5;
  font-size: 40px;
  font-weight: 500;
  cursor: pointer;
  user-select: none;
}

.iconsFooter img {
  width: 25px;
  height: 25px;
}

.textoOscuro {
  color: #130101;
}

.textoClaro {
  color: #f3f4f5;
}

#light {
  position: fixed;
  left: 95%;
}

#light img {
  width: 30px;
  height: 30px;
}

.textDark {
  color: #f3f4f5;
}

.textLight {
  color: #130101;
}

a {
  text-decoration: underline;
  text-underline-offset: 7px;
}

.activeText {
  text-decoration: underline;
  text-underline-offset: 0.1em;
  text-decoration-thickness: 0.1em;
}

.Presentation {
  font-size: 42px;
  font-weight: 500;
}

#imgprincipal {
  width: 500px;
  height: 500px;
  position: absolute;
  left: 60%;
  bottom: 5%;
  border-radius: 8%;
}

#fotoPersonal {
  width: 220px;
  height: 220px;
  border-radius: 50%;
  position: relative;
  object-fit: cover;
}

.underlineText {
  font-size: 19px;
  text-decoration: underline;
  text-underline-offset: 0.2em;
  cursor: pointer;
}

.helloWorld {
  margin: 10px;
  font-size: 35px !important;
  cursor: pointer !important;
}

.animated-text {
  font-size: 4em;
  font-weight: bold;
  background: linear-gradient(90deg, #007acc, #43a047, #f28b25, #a074c4, #e51400);
  background-size: 500% 500%;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientAnimation 10s ease infinite;
}

@keyframes gradientAnimation {
  0% {
    background-position: 0% 50%;
  }
  25% {
    background-position: 50% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  75% {
    background-position: 50% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

#homeButton {
  background-color: #4ecdc4;
  border: none;
  height: 50px;
  width: 50px;
}

 @media(max-width:768px){
  #titles {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  #imgprincipal {
    width: 200px;
    height: 200px;
    position: absolute;
    border-radius: 8%;
    left: 0;
    bottom: 0;
    margin-bottom: 20px;
  }

#light{
 position: fixed;
  left: 80% !important;
}
 

}

@media(max-width:1300px){
  #titles {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  #imgprincipal {
    width: 300px;
    height: 300px;
    position: absolute;
    border-radius: 8%;
    left: 900px;
   top: 400px;
  }
}



/* Responsive Styles */
@media (max-width: 768px) {
  #titles {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  #fotoPersonal {
    width: 150px;
    height: 150px;
  }

  .Presentation {
    font-size: 21px;
  }

  .underlineText {
    font-size: 16px;
  }

  .helloWorld {
    font-size: 24px;
  }

  #imgprincipal {
    width: 200px;
    height: 200px;
    position: static;
    border-radius: 8%;
    left: 0;
    bottom: 0;
    margin-bottom: 20px;

  }

  .menuLightMode,
  .menuDarkMode {
    font-size: 24px;
    margin: 10px 0;
  }

  .footer {
    flex-direction: row;
  }

  #light {
    left: 90%;
  }
  p{
    width: 100%;
  }
}
</style>
