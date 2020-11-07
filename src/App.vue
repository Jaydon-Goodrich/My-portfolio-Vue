<template>
  <div class="backgrounds overlay">
    <div class="background"></div>
  </div>
  <myHeader />
  <myBio />
  <myProject v-bind:projects="projects" />
  <contactMe />
</template>

<script>
import myHeader from "./components/myHeader";
import myBio from "./components/myBio";
import myProject from "./components/myProject";
import contactMe from "./components/contactMe";

export default {
  name: "App",
  components: {
    myHeader,
    myBio,
    myProject,
    contactMe
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "Tech Blog Full Stack",
          url: "https://powerful-beyond-37749.herokuapp.com/",
          bgUrl: require('./assets/techBlogSized.png'),
          isLeft: true
        },
        {
          id: 2,
          title: "Note Taker w/ExpressJs",
          url: "https://peaceful-refuge-43745.herokuapp.com/",
          bgUrl: require('./assets/noteTakerSized.png'),
          isRight: true
        },
        {
          id: 3,
          title: "Game Finder Front End",
          url: "https://jaydon-goodrich.github.io/game-finder/",
          bgUrl: require('./assets/gameFinderSized.png'),
          isLeft: true
        },
        {
          id: 4,
          title: "Employee Tracker NodeJS",
          url: "https://github.com/Jaydon-Goodrich/employee-tracker",
          bgUrl: require('./assets/employeeTrackerSized.png'),
          isRight: true
        },
        {
          id: 5,
          title: "Weather Dashboard w/bootstrap",
          url: "https://jaydon-goodrich.github.io/weather-dashboard/",
          bgUrl: require('./assets/weatherDashboardSized.png'),
          isLeft: true
        },
        {
          id: 6,
          title: "Ecommerce Back End",
          url: "https://github.com/Jaydon-Goodrich/orm-project",
          bgUrl: require('./assets/backendSized.png'),
          isRight: true
        }
      ]
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap");

.backgrounds {
  width: 100%;
  height: 100%;
  position: fixed;
  z-index: -1;
  margin-left: -8px;
  margin-top: -8px;
}
.backgrounds .background {
  width: 100%;
  height: 100%;
  background-size: cover;
  position: absolute;
  left: 0;
  top: 0;
  background-attachment: fixed;
  background-image: url("./assets/port-background.jpg");
}
.overlay:after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  background: black;
  opacity: 0.5;
}
h3 {
  font-family: "Roboto", sans-serif;
  font-size: 150%;
}
</style>
