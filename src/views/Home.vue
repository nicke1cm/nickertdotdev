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
          <h4 class="mt-3">Experience</h4>
          <mdb-card class="mt-3">
            <mdb-list-group>
              <mdb-list-group-item>Prog[in]ress</mdb-list-group-item>
            </mdb-list-group>
          </mdb-card>
          <h4 class="mt-3">Education</h4>
          <mdb-card class="mt-3">
            <mdb-list-group>
              <mdb-list-group-item>Prog[in]ress</mdb-list-group-item>
            </mdb-list-group>
          </mdb-card>
          <h4 class="mt-3">Projects</h4>
          <mdb-card class="mt-3">
            <mdb-list-group>
              <mdb-list-group-item>Prog[in]ress</mdb-list-group-item>
            </mdb-list-group>
          </mdb-card>
        </mdb-col>
        <mdb-col lg="5" xl="4">
          <div class="sticky-top pt-5 pb-4">
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
import JobPostingModal from "@/components/JobPostingModal.vue";
import CoverLetterModal from "@/components/CoverLetterModal.vue";
import {
  mdbCard,
  mdbContainer,
  mdbRow,
  mdbCol,
  mdbListGroup,
  mdbListGroupItem
  //mdbTooltip
} from "mdbvue";

export default {
  name: "home",
  components: {
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
