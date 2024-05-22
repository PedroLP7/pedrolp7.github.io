<template>
  <div>
    <div class="objectivesDiv">
      <p class="titlesKnow" :class="{ textLight: lights, textDark: !lights }">{{ objetivos }}</p>
      <img class="imgDet" src="../assets/objetivos.png" alt="">

      <p :class="{ textLight: lights, textDark: !lights }">
        {{ objetivosTxt }}
      </p>
      <button class="btn btn-warning animacion" v-if="!showHobbies" @click="showInterests()">Show More</button>
    </div>

    <div v-if="showHobbies" class="interestsDiv">
      <p class="titlesKnow" :class="{ textLight: lights, textDark: !lights }">{{ intereses }}</p>
      <img class="imgDet" src="../assets/interests1.jpg" alt="">

      <p :class="{ textLight: lights, textDark: !lights }">
        {{ interesesTxt1 }}
      </p>

      <p id="texttoJump1" :class="{ textLight: lights, textDark: !lights }">
        {{ interesesTxt2 }}
      </p>
      <button class="btn btn-warning animacion" v-if="!showSkills" @click="showSkillstxt()">Show More</button>
    </div>

    <div v-if="showSkills" class="skillsDiv">
      <p class="titlesKnow" :class="{ textLight: lights, textDark: !lights }">{{ habilidades }}</p>
      <img class="imgDet" src="../assets/skills.jpg" alt="">
      <p :class="{ textLight: lights, textDark: !lights }">
        {{ skillsTxt }}
      </p>
      <p :class="{ textLight: lights, textDark: !lights }">
        {{ skillTxt2 }}
      </p>
      <p :class="{ textLight: lights, textDark: !lights }">
        {{ skillTxt3 }}
      </p>
      <p id="texttoJump2" :class="{ textLight: lights, textDark: !lights }">
        {{ skillTxt4 }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Aboutme",
  data() {
    return {
      showHobbies: false,
      showSkills: false,
    };
  },
  props: {
    language: String,
    lights: Boolean,
  },
  computed: {
    objetivos() {
      return this.language === "english"
        ? "Professional Objectives"
        : this.language === "spanish"
        ? "Objetivos Profesionales"
        : this.language === "catalan"
        ? "Objectius Professionals"
        : "Professional Objectives";
    },
    intereses() {
      return this.language === "english"
        ? "Hobbies And Interests"
        : this.language === "spanish"
        ? "Gustos Y Aficiones"
        : this.language === "catalan"
        ? "Aficions I Interessos"
        : "Hobbies And Interests";
    },
    habilidades() {
      return this.language === "english"
        ? "Skills"
        : this.language === "spanish"
        ? "Habilidades"
        : this.language === "catalan"
        ? "Habilitats"
        : "Skills";
    },
    objetivosTxt() {
      return this.language === "english"
        ? "My main goal is to find a job as a backend web developer while continuing to train in more technologies and programming languages. I am passionate about web development and I am determined to improve my skills and knowledge in this area to contribute effectively to challenging and dynamic projects. I am constantly looking for opportunities to learn and grow professionally, whether through courses, workshops or personal projects."
        : this.language === "spanish"
        ? "Mi principal objetivo es encontrar un trabajo como desarrollador web backend mientras continúo formándome en más tecnologías y lenguajes de programación. Me apasiona el desarrollo web y estoy decidido a mejorar mis habilidades y conocimientos en esta área para contribuir eficazmente en proyectos desafiantes y dinámicos. Estoy constantemente buscando oportunidades para aprender y crecer profesionalmente, ya sea a través de cursos, talleres o proyectos personales."
        : this.language === "catalan"
        ? "El meu principal objectiu es trobar feina com a desenvolupador web backend mentre continuo formant-me en més tecnologies i llenguatges de programació. M'apassiona el desenvolupament web i estic decidit a millorar les meves habilitats i coneixements en aquesta àrea per contribuir eficaçment en projectes desafiants i dinàmics. Estic constantment buscant oportunitats per aprendre i créixer professionalment, ja sigui a través de cursos, tallers o projectes personals."
        : "My main goal is to find a job as a backend web developer while continuing to train in more technologies and programming languages. I am passionate about web development and I am determined to improve my skills and knowledge in this area to contribute effectively to challenging and dynamic projects. I am constantly looking for opportunities to learn and grow professionally, whether through courses, workshops or personal projects.";
    },
    interesesTxt1() {
      return this.language === "english"
        ? "Outside of work, I have a great passion for video games, PC hardware and technology in general. Video games are not only a source of entertainment for me, but also a constant inspiration to better understand the interaction between software and the user. In addition, I enjoy exploring and experimenting with different hardware components, which allows me to stay up to date with the latest technological innovations and improve my own PC setups."
        : this.language === "spanish"
        ? "Fuera del ámbito profesional, tengo una gran pasión por los videojuegos, el hardware de PC y la tecnología en general. Los videojuegos no solo son una fuente de entretenimiento para mí, sino también una inspiración constante para entender mejor la interacción entre el software y el usuario. Además, disfruto explorando y experimentando con diferentes componentes de hardware, lo que me permite mantenerme al día con las últimas innovaciones tecnológicas y mejorar mis propias configuraciones de PC."
        : this.language === "catalan"
        ? "Fora de l'àmbit professional, tinc una gran passió pels videojocs, el hardware de PC i la tecnologia en general. Els videojocs no només són una font d'entreteniment per a mi, sinó també una inspiració constant per entendre millor la interacció entre el programari i l'usuari. A més, gaudeixo explorant i experimentant amb diferents components de hardware, el que em permet mantenir-me al dia amb les últimes innovacions tecnològiques i millorar les meves pròpies configuracions de PC."
        : "Outside of work, I have a great passion for video games, PC hardware and technology in general. Video games are not only a source of entertainment for me, but also a constant inspiration to better understand the interaction between software and the user. In addition, I enjoy exploring and experimenting with different hardware components, which allows me to stay up to date with the latest technological innovations and improve my own PC setups.";
    },
    interesesTxt2() {
      return this.language === "english"
        ? "Another of my great passions is sports, especially weightlifting at the gym. I love staying active and improving my physical condition, which not only benefits my health, but also helps me develop discipline and consistency, qualities that I consider very valuable both in my personal and professional life."
        : this.language === "spanish"
        ? "Otra de mis grandes aficiones es el deporte, especialmente la musculación en el gimnasio. Me encanta mantenerme activo y mejorar mi condición física, lo que no solo beneficia mi salud, sino que también me ayuda a desarrollar disciplina y constancia, cualidades que considero muy valiosas tanto en mi vida personal como profesional."
        : this.language === "catalan"
        ? "Una altra de les meves grans aficions és l'esport, especialment la musculació al gimnàs. M'encanta mantenir-me actiu i millorar la meva condició física, el que no només beneficia la meva salut, sinó que també m'ajuda a desenvolupar disciplina i constància, qualitats que considero molt valuoses tant en la meva vida personal com professional."
        : "Another of my great passions is sports, especially weightlifting at the gym. I love staying active and improving my physical condition, which not only benefits my health, but also helps me develop discipline and consistency, qualities that I consider very valuable both in my personal and professional life.";
    },
    skillsTxt() {
      return this.language === "english"
        ? "Teamwork: I highly value collaboration and effective communication within a team. I firmly believe that working together and synergy are key to the success of any project."
        : this.language === "spanish"
        ? "Trabajo en equipo: Valoro enormemente la colaboración y la comunicación efectiva dentro de un equipo. Creo firmemente que el trabajo conjunto y la sinergia son claves para el éxito de cualquier proyecto."
        : this.language === "catalan"
        ? "Treball en equip: Valoro enormement la col·laboració i la comunicació efectiva dins d'un equip. Crec fermament que el treball conjunt i la sinergia són claus per a l'èxit de qualsevol projecte."
        : "Teamwork: I highly value collaboration and effective communication within a team. I firmly believe that working together and synergy are key to the success of any project.";
    },
    skillTxt2() {
      return this.language === "english"
        ? "Self-taught: I have a strong ability to learn independently. I am always in search of new knowledge and I strive to stay up to date with the latest web development technologies and methodologies."
        : this.language === "spanish"
        ? "Autodidacta: Tengo una fuerte capacidad para aprender de forma independiente. Siempre estoy en la búsqueda de nuevos conocimientos y me esfuerzo por mantenerme actualizado con las últimas tecnologías y metodologías del desarrollo web."
        : this.language === "catalan"
        ? "Autodidacta: Tinc una forta capacitat per aprendre de forma independent. Sempre estic en la recerca de nous coneixements i em esforço per mantenir-me actualitzat amb les últimes tecnologies i metodologies del desenvolupament web."
        : "Self-taught: I have a strong ability to learn independently. I am always in search of new knowledge and I strive to stay up to date with the latest web development technologies and methodologies.";
    },
    skillTxt3() {
      return this.language === "english"
        ? "Discipline: I am a very disciplined and committed person in my work. This discipline allows me to manage my time efficiently, meet deadlines and maintain a high standard of quality in everything I do."
        : this.language === "spanish"
        ? "Disciplina: Soy una persona muy disciplinada y comprometida con mi trabajo. Esta disciplina me permite gestionar mi tiempo de manera eficiente, cumplir con los plazos y mantener un alto estándar de calidad en todo lo que hago."
        : this.language === "catalan"
        ? "Disciplina: Sóc una persona molt disciplinada i compromesa amb la meva feina. Aquesta disciplina em permet gestionar el meu temps de manera eficient, complir amb els terminis i mantenir un alt estàndard de qualitat en tot el que faig."
        : "Discipline: I am a very disciplined and committed person in my work. This discipline allows me to manage my time efficiently, meet deadlines and maintain a high standard of quality in everything I do.";
    },
    skillTxt4() {
      return this.language === "english"
        ? "This skills, along with my passion for technology and my continuous desire for learning, make me an ideal candidate for a backend web developer position. I am excited for the opportunities that the future holds for me and ready to face new challenges in the world of web development."
        : this.language === "spanish"
        ? "Estas habilidades, junto con mi pasión por la tecnología y mi deseo continuo de aprendizaje, me convierten en un candidato ideal para un puesto de desarrollador web backend. Estoy emocionado por las oportunidades que el futuro me depara y listo para enfrentar nuevos retos en el mundo del desarrollo web."
        : this.language === "catalan"
        ? "Aquestes habilitats, juntament amb la meva passió per la tecnologia i el meu desig continu de l'aprenentatge, em converteixen en un candidat ideal per a un lloc de desenvolupador web backend. Estic emocionat per les oportunitats que el futur em depara i llest per enfrontar nous reptes en el món del desenvolupament web."
        : "This skills, along with my passion for technology and my continuous desire for learning, make me an ideal candidate for a backend web developer position. I am excited for the opportunities that the future holds for me and ready to face new challenges in the world of web development.";
    }
  },
  methods: {
    showInterests() {
      this.showHobbies = true;
      this.$nextTick(() => {
        const textElement = document.getElementById('texttoJump1');
        textElement.scrollIntoView({ behavior: 'smooth' });
      });
    },
    showSkillstxt() {
      this.showSkills = true;
      this.$nextTick(() => {
        const textElement = document.getElementById('texttoJump2');
        textElement.scrollIntoView({ behavior: 'smooth' });
      });
    }
  }
};
</script>

<style scoped>
p {
  font-size: 20px;
  margin: 20px;
  width: 50%;
}

.imgDet {
  float: right;
  width: 200px;
  height: 200px;
  margin-right: 250px;
  border-radius: 50%;
}

#texttoJump2 {
  margin-bottom: 100px;
}

.btn-warning {
  background-color: #4ECDC4;
  color: white;
  margin-left: 20px;
  border: none;
}
.btn-warning:hover {
  background-color: #4ECDC4;
  color: white;
  transform: scale(1.1);
}

.titlesKnow {
  font-size: 30px;
  margin: 20px;
  width: 50%;
  text-align: center;
  text-decoration: underline;
  text-underline-offset: 0.2em !important;
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

.objectivesDiv,
.interestsDiv,
.skillsDiv {
  margin-top: 50px;
  margin-bottom: 50px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 1px solid #4ECDC4;
  border-radius: 10px;
  padding: 20px;
  width: 80%;
  margin-left: 10%;
  margin-right: 10%;
  box-shadow: 0 0 10px #4ECDC4;
}

@media screen and (max-width: 768px) {
  p {
    width: 90%;
    font-size: 16px;
  }

  .imgDet {
    float: none;
    width: 100px;
    height: 100px;
    margin: 0 auto;
    display: block;
  }

  .btn-warning {
    margin-left: 0;
    display: block;
    width: auto;
    margin-top: 20px;
  }

  .titlesKnow {
    width: 100%;
    font-size: 24px;
  }

  .objectivesDiv,
  .interestsDiv,
  .skillsDiv {
    width: 90%;
    margin-left: 5%;
    margin-right: 5%;
  }
}
</style>
