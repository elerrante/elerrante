<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Mateo Castilla Matallana</h3>
                  <h6>Web Developer</h6>
                  <md-button
                    href="https://www.linkedin.com/in/elerrante"
                    class="md-just-icon md-simple md-dribbble"
                    ><i class="fab fa-linkedin"></i
                  ></md-button>
                  <md-button
                    href="https://github.com/elerrante"
                    class="md-just-icon md-simple md-twitter"
                    ><i class="fab fa-github"></i
                  ></md-button>
                  <md-button
                    href="https://api.whatsapp.com/send?phone=573162270432"
                    class="md-just-icon md-simple md-pinterest"
                    ><i class="fab fa-whatsapp"></i
                  ></md-button>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
             Hi! I'm _Elerrante, from Cali-Colombia, 26 years old. <br> I'm a web developer with ability to adapt in every collaborative
             enviroment while staying focused on achieving high quality results. This drove me to work on personal and proffesional projects. Such projects have taught
             me to have a strong mentality. I've studied Computer Science Engeneering and Industrial Engeneering (VI Semester) in University of La Sabana. <br><br>
             I love playing and whatching soccer matches, I like having easy times with family and friends, like whatching series and movies. I'm a cat lover.
            </p>
            <br>
            <div>
            <h3 style="color: black;" >Skills</h3>
            
            <h3>JavaScript</h3>
             <md-progress-bar
            class="md-info"
            :md-value="javascript"
          ></md-progress-bar>

           <h3>VueJS</h3>
             <md-progress-bar
            class="md-info"
            :md-value="vuejs"
          ></md-progress-bar>

           <h3>React</h3>
             <md-progress-bar
            class="md-info"
            :md-value="react"
          ></md-progress-bar>

           <h3>Angular</h3>
             <md-progress-bar
            class="md-info"
            :md-value="angular"
          ></md-progress-bar>

            <h3>Scrum</h3>
             <md-progress-bar
            class="md-info"
            :md-value="scrum"
          ></md-progress-bar>

            <h3>Heroku - AWS</h3>
             <md-progress-bar
            class="md-info"
            :md-value="heroku"
          ></md-progress-bar>

            <h3>PHP Laravel</h3>
             <md-progress-bar
            class="md-info"
            :md-value="php"
          ></md-progress-bar>

           <h3>NodeJS</h3>
             <md-progress-bar
            class="md-info"
            :md-value="node"
          ></md-progress-bar>

            </div>

          <br>
            <div>
            <h3 style="color: black;" >Work History</h3>

                 <div class="profile-tabs">
            <tabs
              :tab-name="['Tax & Legal', 'Geca Group', 'VOZ']"
              :tab-icon="['', '', '']"
              plain
              nav-pills-icons
              color-button="info"
            >
              <!-- here you can add your content for tab-content -->
              <template slot="tab-pane-1">
                <div class="md-layout">
                  <div class="md-layout-item  ml-auto">
                    
                    <p>ADMINISTRATIVE AND TECH ASSISTANT</p>
                    <p>2014 – Jan. 2016</p>
                    <ul>
                      <li>Managed and improved the technological infrastructure acquired.</li>
                      <li>Developed and deployed the official website using Bootstrap.</li>
                    </ul>
                  </div>
                </div>
              </template>
              <template slot="tab-pane-2">
                <div class="md-layout">
                  <div class="md-layout-item ml-auto">
                    <p>FREELANCER</p>
                    <p>JAN. 2016 – MAr. 2018</p>
                    <ul>
                      <li>Sold websites and community management services.</li>
                      <li>Managed social media (Instagram, Facebook) for clients from different sectors.</li>
                      <li>Produced static web and mobile apps, using Bootstrap, CSS and Android Studio.</li>
                   </ul>
                  </div>
                </div>
              </template>
              <template slot="tab-pane-3">
                <div class="md-layout">
                  <div class="md-layout-item ml-auto">
                    <p>TECHNICAL MANAGER</p>
                    <p>APR. 2018 – Jan. 2022</p>
                    <ul>
                      <li>Responsible for getting new clients to the company and maintaining the company’s relationship with them.</li>
                      <li>Led and tested the development, deployment and production of the SaaS (Software as a Service) built with PHP-Laravel, NodeJS, Angular and React.</li>
                   </ul>
                   <br>
                    <p>WEB DEVELOPER</p>
                    <p>Feb. 2020 – Jan. 2022</p>
                    <ul>
                      <li>Developed a Front-end project that allows people to create a profile, find profiles, rate profiles and share profiles, built with Vue JS.</li>
                      <li>Deployed a Front-end and Back-end project using Heroku and AWS services.</li>
                      <li>Maintained an SAAS built with PHP-Laravel, Angular and react .</li>

                   </ul>
                  </div>
                </div>
              </template>
            </tabs>
          </div>
            </div>

          </div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>

 import { Tabs } from "@/components";

export default {
 components: {
    Tabs
  },
  bodyClass: "profile-page",
  data() {
    return {
      javascript: 70,
      vuejs: 70,
      react: 70,
      angular: 30,
      node: 30,
      php: 30,
      scrum: 50,
      heroku: 50,
       
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/mateo.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}

.profile-tabs::v-deep {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
