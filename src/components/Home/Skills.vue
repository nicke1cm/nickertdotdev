<template>
  <div class="skills">
    <mdb-card class="mt-2">
      <mdb-list-group>
        <mdb-list-group-item>
          <div class="d-flex flex-column flex-lg-row justify-content-around w-100">
            <div>
              <i class="fab fa-java mr-1"></i>Java
            </div>
            <div>
              <i class="fas fa-leaf mr-1"></i>Spring Boot
            </div>
            <div>
              <i class="fas fa-database mr-1"></i>SQL & JPA
            </div>
            <div>
              <i class="fab fa-js mr-1"></i>JavaScript
            </div>
            <div>
              <i class="fab fa-react mr-1"></i>React.js
            </div>
            <div>
              <i class="fab fa-vuejs mr-1"></i>Vue.js
            </div>
          </div>
        </mdb-list-group-item>
        <mdb-list-group-item>
          <div class="d-flex flex-row justify-content-between w-100">
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Android</span>
              <a slot="reference">
                <i class="fab fa-android"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">npm</span>
              <a slot="reference">
                <i class="fab fa-npm"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Node.js</span>
              <a slot="reference">
                <i class="fab fa-node"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">HTML</span>
              <a slot="reference">
                <i class="fab fa-html5"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">CSS</span>
              <a slot="reference">
                <i class="fab fa-css3"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Bootstrap</span>
              <a slot="reference">
                <i class="fab fa-bootstrap"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Material Design for Bootstrap</span>
              <a slot="reference">
                <i class="fab fa-mdb"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Jenkins CI/CD</span>
              <a slot="reference">
                <i class="fab fa-jenkins"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">GitHub</span>
              <a slot="reference">
                <i class="fab fa-github"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">git</span>
              <a slot="reference">
                <i class="fab fa-git-alt"></i>
              </a>
            </mdb-tooltip>
            <mdb-tooltip trigger="hover" :options="{placement: 'bottom'}">
              <span slot="tip">Linux</span>
              <a slot="reference">
                <i class="fab fa-linux"></i>
              </a>
            </mdb-tooltip>
          </div>
        </mdb-list-group-item>
      </mdb-list-group>
    </mdb-card>
  </div>
</template>

<script>
import { mdbCard, mdbListGroup, mdbListGroupItem, mdbTooltip } from "mdbvue";
export default {
  name: "Skills",
  components: {
    mdbCard,
    mdbListGroup,
    mdbListGroupItem,
    mdbTooltip
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
</style>
