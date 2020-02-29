<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <Hero />
    <mdb-container fluid class="cloudy-knoxville-gradient pb-3">
      <mdb-row>
        <mdb-col col="sm" class="pt-3">
          <h4>Skills</h4>
          <Skills />
          <h4 class="mt-3">Education</h4>
          <Education />
          <h4 class="mt-3">Experience</h4>
          <mdb-card class="mt-3">
            <mdb-list-group>
              <mdb-list-group-item>
                <img
                  src="../assets/ford.png"
                  class="img-fluid z-depth-1 rounded-circle mr-3"
                  alt="Ford Motor Company"
                  width="50px"
                />
                <div class="w-100">
                  <div class="d-flex justify-content-between">
                    <div class="text-left">
                      <strong>Ford Motor Company</strong>
                      <small class="ml-2">Dearborn, MI</small>
                    </div>
                    <!-- <div>2018 - Present</div> -->
                  </div>
                  <div class="d-flex justify-content-between">
                    <span class="font-weight-lighter">
                      Software Engineer
                      <a href="#">
                        <i class="fas fa-info-circle"></i>
                      </a>
                    </span>
                    <span>2019 - now</span>
                  </div>
                  <div class="d-flex justify-content-between">
                    <span class="font-weight-lighter">
                      Junior Software Engineer
                      <a href="#">
                        <i class="fas fa-info-circle"></i>
                      </a>
                    </span>
                    <span>2018 - 2019</span>
                  </div>
                </div>
              </mdb-list-group-item>
              <mdb-list-group-item>
                <img
                  src="../assets/gfs.png"
                  class="img-fluid z-depth-1 rounded-circle mr-3"
                  alt="Gordon Food Service"
                  width="50px"
                />
                <div class="w-100">
                  <div class="d-flex justify-content-between">
                    <div class="text-left">
                      <strong>Gordon Food Service</strong>
                      <small class="ml-2">Grand Rapids, MI</small>
                    </div>
                    <!-- <div>2018 - Present</div> -->
                  </div>
                  <div class="d-flex justify-content-between">
                    <span class="font-weight-lighter">Software Development Intern</span>
                    <span>2017</span>
                  </div>
                </div>
              </mdb-list-group-item>
            </mdb-list-group>
          </mdb-card>
          <h4 class="mt-3">Projects</h4>
          <Projects />

          <!-- <mdb-card class="mt-3">
            <mdb-list-group>
              <mdb-list-group-item style="padding-top: 56.25%;">
                <iframe
                  width="100%"
                  height="100%"
                  src="https://www.youtube-nocookie.com/embed/5V3P3icn12U?controls=0"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                  style="border-radius: .3em;  position: absolute;   top: 0; left: 0; bottom: 0; right: 0;"
                ></iframe>
              </mdb-list-group-item>
            </mdb-list-group>
          </mdb-card>-->
        </mdb-col>
        <mdb-col lg="5" xl="4">
          <div class="sticky-top pt-5">
            <div class="card" style="width: fit-content; margin: auto;">
              <LinkedInBox />
            </div>
            <mdb-card class="mt-3" style="width: 330px; margin: auto;">
              <mdb-list-group>
                <mdb-list-group-item>
                  <a v-on:click="showJobPostingModal">
                    <i class="fas fa-briefcase mr-2"></i>Send Me a Job Posting
                  </a>
                  <JobPostingModal
                    v-bind:poll="jobPostingModalToggle"
                    @jobPostingModalToggleEmit="jobPostingModalToggle = $event"
                  />
                </mdb-list-group-item>
              </mdb-list-group>
            </mdb-card>
            <mdb-card class="mt-3" style="width: 330px; margin: auto;">
              <mdb-list-group>
                <mdb-list-group-item>
                  <a v-on:click="showCoverLetterModal">
                    <i class="fas fa-file-signature mr-2"></i>Generate Unique Cover Letter
                  </a>
                  <CoverLetterModal
                    v-bind:poll="coverLetterModalToggle"
                    @coverLetterModalToggleEmit="coverLetterModalToggle = $event"
                  />
                </mdb-list-group-item>
              </mdb-list-group>
            </mdb-card>
            <mdb-card class="mt-3" style="width: 330px; margin: auto;">
              <mdb-list-group>
                <mdb-list-group-item>
                  <a>
                    <i class="fas fa-file-download mr-2"></i>Download My Resume
                  </a>
                </mdb-list-group-item>
              </mdb-list-group>
            </mdb-card>
          </div>
        </mdb-col>
      </mdb-row>
      <hr class="mt-5 mb-5" />
      <mdb-row>
        <mdb-col class="pb-4">
          <div>
            <h3 class="code pink-text">Let's Get Personal</h3>
          </div>
          <mdb-btn color="pink">About Me</mdb-btn>
          <mdb-btn color="pink">My Blog</mdb-btn>
          <div>
            <small class="code">Learn a little bit more about me.</small>
          </div>
        </mdb-col>
      </mdb-row>
    </mdb-container>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import Hero from "@/components/Home/Hero.vue";
import LinkedInBox from "@/components/LinkedInBox/LinkedInBox";
import Footer from "@/components/Footer.vue";
import Skills from "@/components/Home/Skills";
import Projects from "@/components/Home/Projects";
import Education from "@/components/Home/Education";
import JobPostingModal from "@/components/JobPostingModal.vue";
import CoverLetterModal from "@/components/CoverLetterModal.vue";
import {
  mdbBtn,
  mdbCard,
  mdbContainer,
  mdbRow,
  mdbCol,
  mdbListGroup,
  mdbListGroupItem,
  animateOnScroll
  //mdbTooltip
} from "mdbvue";

export default {
  name: "home",
  directives: {
    animateOnScroll
  },
  components: {
    mdbBtn,
    mdbCard,
    mdbContainer,
    mdbRow,
    mdbCol,
    mdbListGroup,
    mdbListGroupItem,
    //mdbTooltip,
    Hero,
    LinkedInBox,
    Footer,
    Skills,
    Education,
    Projects,
    JobPostingModal,
    CoverLetterModal
  },
  data: () => {
    return {
      jobPostingModalToggle: false,
      coverLetterModalToggle: false,
      modalToggledAtLeastOnce: false
    };
  },
  created: function() {
    setTimeout(() => {
      if (!this.modalToggledAtLeastOnce) {
        this.showJobPostingModal();
      }
    }, 30000);
  },
  methods: {
    showJobPostingModal: function() {
      this.jobPostingModalToggle = true;
    },
    showCoverLetterModal: function() {
      this.coverLetterModalToggle = true;
    }
  },
  watch: {
    jobPostingModalToggle: function() {
      this.modalToggledAtLeastOnce = true;
    },
    coverLetterModalToggle: function() {
      this.modalToggledAtLeastOnce = true;
    }
  }
};
</script>

<style scoped lang="scss">
.home {
  height: 100%;
}
</style>
