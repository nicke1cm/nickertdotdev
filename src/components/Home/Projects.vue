<template>
  <div class="projects">
    <mdb-card class="mt-3">
      <mdb-list-group>
        <mdb-list-group-item>
          <div class="w-100 d-block">
            <div class="pink-text link" v-on:click="currentOpenPanels = '0123456789'">Expand All</div>
            <div class="d-flex mt-2">
              <mdb-card-body class="m-0 p-0">
                <a v-on:click="openPanel(0)" class="d-flex justify-content-between">
                  <div>
                    <img
                      src="/favicon.png"
                      class="img-fluid z-depth-1 rounded-circle mr-3"
                      alt="Myself"
                      width="50px"
                    />
                    <strong>This Website</strong>
                  </div>
                  <div>
                    <span>Jan 2020 – Present</span>
                    <i
                      :class="isPanelOpen(0)? 'fa-chevron-up': 'fa-chevron-down'"
                      class="pink-text ml-3 fas fa-2x"
                    ></i>
                  </div>
                </a>
                <div :class="isPanelOpen(0)? 'open': 'closed'" class="accordion-body">
                  <mdb-card-text
                    class="pt-4"
                  >Created a full-stack resume website where recruiters can see a live demo of my qualifications. The site features the ability for users to send me job openings, generate unique cover letters, and download my resume. (Java, Spring Boot, Vue.js, JavaScript, Bootstrap, Heroku, npm, gradle).</mdb-card-text>
                  <a href="#">View Project</a>
                </div>
              </mdb-card-body>
            </div>
          </div>
        </mdb-list-group-item>

        <mdb-list-group-item>
          <mdb-card-body class="m-0 p-0">
            <a v-on:click="openPanel(1)" class="d-flex justify-content-between">
              <div>
                <img
                  src="../../assets/ford.png"
                  class="img-fluid z-depth-1 rounded-circle mr-3"
                  alt="Ford Motor Company"
                  width="50px"
                />
                <strong>Ford Payment Library</strong>
              </div>
              <div>
                <span>Apr 2019 – Present</span>
                <i
                  :class="isPanelOpen(1)? 'fa-chevron-up': 'fa-chevron-down'"
                  class="pink-text ml-3 fas fa-2x"
                ></i>
              </div>
            </a>
            <div :class="isPanelOpen(1)? 'open': 'closed'" class="accordion-body">
              <mdb-card-text
                class="pt-4"
              >I lead in creating an embedded library that enables other Ford teams to accept credit card payments from customers through the web. This enables customers to securely pay for future mobility services within the Ford ecosystem. Currently, customers can reserve a pre-configured Mustang Mach-E online. The website uses the library to drive millions of dollars in transactions. (React.js, JavaScript, Java, Spring Boot, Bootstrap, jQuery, npm, gradle, PCF, Jenkins, and Postman).</mdb-card-text>
              <a href="https://www.ford.com/buy/mach-e/build-and-price.html#/model" target="_blank">
                View Project
                <i class="fas fa-external-link-alt"></i>
              </a>
            </div>
          </mdb-card-body>
        </mdb-list-group-item>

        <mdb-list-group-item>
          <mdb-card-body class="m-0 p-0">
            <a v-on:click="openPanel(2)" class="d-flex justify-content-between">
              <div>
                <img
                  src="../../assets/uofm.png"
                  class="img-fluid z-depth-1 rounded-circle mr-3"
                  alt="University of Michigan"
                  width="50px"
                />
                <strong>Kanboard Task Manager</strong>
              </div>
              <div>
                <span>Oct 2019 – Dec 2019</span>
                <i
                  :class="isPanelOpen(2)? 'fa-chevron-up': 'fa-chevron-down'"
                  class="pink-text ml-3 fas fa-2x"
                ></i>
              </div>
            </a>
            <div :class="isPanelOpen(2)? 'open': 'closed'" class="accordion-body">
              <mdb-card-text
                class="pt-4"
              >ECE 574 - The project outlines an iterative agile software engineering method in order to create a Kanban board web application called Kanboard. The project features user management and the ability to mangae the project tasks (React.js, Java, Spring Boot, Bootstrap, JavaScript, jQuery, npm, gradle, SQL, JPA, Heroku, and Postman).</mdb-card-text>
              <a href="https://u-of-m-kanboard-spa.herokuapp.com/" target="_blank">
                View Project
                <i class="fas fa-external-link-alt"></i>
              </a>
            </div>
          </mdb-card-body>
        </mdb-list-group-item>
      </mdb-list-group>
    </mdb-card>
  </div>
</template>

<script>
import {
  mdbCard,
  mdbCardText,
  mdbCardBody,
  mdbListGroup,
  mdbListGroupItem
} from "mdbvue";
export default {
  name: "Projects",
  components: {
    mdbCard,
    mdbCardText,
    mdbCardBody,
    mdbListGroup,
    mdbListGroupItem
  },
  data: () => {
    return {
      currentOpenPanels: ""
    };
  },
  methods: {
    openPanel: function(panelIndex) {
      if (this.isPanelOpen(panelIndex)) {
        this.currentOpenPanels = this.currentOpenPanels.replace(
          panelIndex.toString(),
          ""
        );
      } else {
        this.currentOpenPanels += panelIndex;
      }
    },
    isPanelOpen: function(panelIndex) {
      return this.currentOpenPanels.indexOf(panelIndex.toString()) > -1;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.accordion-body {
  transition: max-height 0.3s linear;
}

.accordion:hover {
  background-color: black;
}

.closed {
  max-height: 0px;
  overflow: hidden;
}

.open {
  max-height: 400px;
  overflow: hidden;
}
</style>
