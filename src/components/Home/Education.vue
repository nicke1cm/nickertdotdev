<template>
  <div class="education">
    <mdb-card class="mt-3">
      <mdb-list-group>
        <div>
          <mdb-list-group-item>
            <img
              src="../../assets/uofm.png"
              class="img-fluid z-depth-1 rounded-circle mr-3"
              alt="University of Michigan"
              width="50px"
            />
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
        <div>
          <mdb-list-group-item>
            <img
              src="../../assets/cmu.png"
              class="img-fluid z-depth-1 rounded-circle mr-3"
              alt="Central Michigan University"
              width="50px"
            />
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
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
</style>
