<template>
  <div class="education">
    <mdb-card class="mt-3">
      <mdb-list-group>
        <div v-on:mouseover="enterUOfM" v-on:mouseleave="leaveUOfM">
          <mdb-list-group-item>
            <div
              class="z-depth-1 rounded-circle mr-3 animated infinite uofm-logo"
              alt="University of Michigan"
              v-bind:class="{ heartBeat: hover1 }"
            >
              <div
                class="h-100 w-100 d-flex rounded-circle animated bg-white"
                alt="Playing Fight Song"
                v-bind:class="{ fadeIn: hover1, fadeOut: !hover1}"
              >
                <i class="fas fa-music fa-2x pink-text m-auto"></i>
              </div>
            </div>
            <div class="w-100">
              <div class="d-flex justify-content-between">
                <div class="text-left">
                  <strong>University of Michigan</strong>
                  <small class="ml-2">Dearborn, MI</small>
                </div>
                <i class="far fa-clock"></i>
              </div>
              <div class="d-flex justify-content-between">
                <span class="font-weight-lighter">M.S. Software Engineering</span>
                <div>2019 - 2020</div>
              </div>
            </div>
          </mdb-list-group-item>
        </div>
        <div v-on:mouseover="enterCMU" v-on:mouseleave="leaveCMU">
          <mdb-list-group-item>
            <div
              class="z-depth-1 rounded-circle mr-3 animated infinite cmu-logo"
              alt="Central Michigan University"
              v-bind:class="{ heartBeat: hover2}"
            >
              <div
                class="h-100 w-100 d-flex rounded-circle animated bg-white"
                alt="Playing Fight Song"
                v-bind:class="{ fadeIn: hover2, fadeOut: !hover2}"
              >
                <i class="fas fa-music fa-2x pink-text m-auto"></i>
              </div>
            </div>
            <div class="w-100">
              <div class="d-flex justify-content-between">
                <div class="text-left">
                  <strong>Central Michigan University</strong>
                  <small class="ml-2">Mt. Pleasant, MI</small>
                </div>
                <i class="fas fa-graduation-cap"></i>
              </div>
              <div class="d-flex justify-content-between">
                <span class="font-weight-lighter">B.S. Computer Science</span>
                <div>2014 - 2018</div>
              </div>
            </div>
          </mdb-list-group-item>
        </div>
      </mdb-list-group>
    </mdb-card>
  </div>
</template>

<script>
let cmuAudio = new Audio("/CMU_Fight_Central.mp3");
let uOfMAudio = new Audio("/UOFM_Victors.mp3");

import {
  mdbCard,
  mdbListGroup,
  mdbListGroupItem
  //mdbTooltip
} from "mdbvue";
export default {
  name: "Education",
  components: {
    mdbCard,
    mdbListGroup,
    mdbListGroupItem
    //    mdbTooltip
  },
  data: () => {
    return { hover1: false, hover2: false };
  },
  methods: {
    enterUOfM: function() {
      this.hover1 = true;
      uOfMAudio.volume = 0.1;
      uOfMAudio.loop = true;
      uOfMAudio.play();
    },
    leaveUOfM: function() {
      this.hover1 = false;
      uOfMAudio.pause();
    },
    enterCMU: function() {
      this.hover2 = true;
      cmuAudio.volume = 0.1;
      cmuAudio.loop = true;
      cmuAudio.play();
    },
    leaveCMU: function() {
      this.hover2 = false;
      cmuAudio.pause();
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.uofm-logo {
  width: 50px;
  height: 50px;
  background-size: 50px 50px;
  background-image: url("../../assets/uofm.png");
  background-position: 50% 50%;
}

.cmu-logo {
  width: 50px;
  height: 50px;
  background-size: 50px 50px;
  background-image: url("../../assets/cmu.png");
  background-position: 50% 50%;
}

</style>
